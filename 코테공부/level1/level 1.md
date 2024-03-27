
- 정수 `n`이 주어질 때, `n`이하의 짝수를 모두 더한 값을 return 하도록 solution 함수를 작성해주세요.

```
function solution(n) {
    let answer = 0;
    for (let i=0; i <= n; i+=2){
        answer += i;
    }
    return answer;
}
```


![[Pasted Graphic 1.png]]


![[[ 자바스크립트 ] Math.floor().png]]




정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.


```
function solution(numbers) {
    let sum = 0;
    for(let i=0; i<numbers.length; i++){
        sum =sum +numbers[i];
    }
    let answer = sum / numbers.length;
    
    return answer;
}
```


머쓱이네 양꼬치 가게는 10인분을 먹으면 음료수 하나를 서비스로 줍니다. 양꼬치는 1인분에 12,000원, 음료수는 2,000원입니다. 정수 `n`과 `k`가 매개변수로 주어졌을 때, 양꼬치 `n`인분과 음료수 `k`개를 먹었다면 총얼마를 지불해야 하는지 return 하도록 solution 함수를 완성해보세요.
```
function solution(n, k) {
    let yang = 12000;
    let bevarage = 2000;
    let service = Math.floor(n/10) ;
    let answer = yang*n + bevarage*(k-service);
    return answer;
}
```



어떤 세균은 1시간에 두배만큼 증식한다고 합니다. 처음 세균의 마리수 `n`과 경과한 시간z `t`가 매개변수로 주어질 때 `t`시간 후 세균의 수를 return하도록 solution 함수를 완성해주세요.

```
function solution(n, t) {
    let bunsik = n*(2**t)
    return bunsik;
}
```