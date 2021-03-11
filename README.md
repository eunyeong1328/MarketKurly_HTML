# 로또 번호 생성
```
import kotlin.random.Random
import java.util.*

fun ran() : List<Int> {//7개의 랜덤숫자 생성
    val lottoNum = mutableListOf<Int>()
    while(lottoNum.size<7){
        val ranNum = Random.nextInt(1,46)
        if(lottoNum.contains(ranNum)){
            continue
        }
        lottoNum.add(ranNum)
    }
    return lottoNum
}
                            
fun main(args: Array<String>){
    println("로또 번호 횟수 입력!!")
    val result = Scanner(System.`in`).nextInt()

    for(i in 1..result) {
        for(num in ran()){
            print("$num ")
        }
        println()
    }
}
```

