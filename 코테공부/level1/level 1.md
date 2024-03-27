
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


순서쌍이란 두 개의 숫자를 순서를 정하여 짝지어 나타낸 쌍으로 (a, b)로 표기합니다. 자연수 `n`이 매개변수로 주어질 때 두 숫자의 곱이 `n`인 자연수 순서쌍의 개수를 return하도록 solution 함수를 완성해주세요.

```
function solution(n) {
    var answer = 0;
    for(let i=0; i <=n; i++){
        if(n%i === 0){
            answer ++;
        }
    }
    return answer;
}
```



문자열 배열 `strlist`가 매개변수로 주어집니다. `strlist` 각 원소의 길이를 담은 배열을 retrun하도록 solution 함수를 완성해주세요.
```
function solution(strlist) {
    let answer = [];
    for(let i=0; i < strlist.length; i++){
        answer[i] = strlist[i].length;
    }
    
    return answer;
}
```
- strlist[i]는 배열의 인덱스 번호. 즉 i가 strlist의 배열의 길이보다 작을때까지 반복.
- 만약, strlist  = ['apple', 'banana', 'cherry', 'date']; 이면 배열의 요소의 개수는 4. 하지만 0부터 시작하기 때문에 0, 1, 2, 3까지 반복. `i<4` 이기 때문에 3까지 반복
- answer에 배열요소를 무엇을 넣을꺼냐면, strlist의 인덱스 요소의 길이들을 answer의 인덱스 요소들에 넣을 것이다.

1. 다른 사람의 풀이 
```
function solution(strlist) {
    return strlist.map((el) => el.length)
}
```
- `배열.map((요소, 인덱스, 배열)=>{return 요소});` 
- map 메서드는 배열 내의 모든 요소 각각에 대해 주어진 함수를 호출한 결과를 **새로운 배열로 변환**
- `el`이라는 요소(즉, **strlist 안에 있는 요소**들을 하나 하나 불러옴)에 el의 length들로 새로운 배열을 만든다



---


2. 다른 사람의 풀이 
```
function solution(strlist) { return strlist.reduce((a, b) => [...a, b.length], []) }
```

- `reduce` 함수는 배열의 요소에 대해 지정된 콜백함수를 실행하고 **그 결과를 누적하는 메서드**
- `(a, b) => [...a, b.length]` a는 누적값, b는 현재 요소. a의 초기 값은 빈배열로 사용
- 여기서 `...a`를 쓰는 이유는 `...`이 스프레드 문법인 것임.
- **스프레드 문법**은 배열 또는 *객체의 요소를 추출하여 다른 배열이나 객체에 복사하거나 합칠 때* 사용
- 즉 `...`씀으로써 배열 안의 요소를 추출할 수 있게됨
- a가 빈배열이니까 빈배열 안에 요소가 없잖슴. 그렇기 때문에 추출할 배열 요소 없이 b.l


-   또 다른 예시 
```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; 
const sum1 = numbers.reduce((accumulator, currentNumber) => 
accumulator + currentNumber); 
console.log('sum1 =', sum1);
```

- numbers라는 배열이 있을때, reduce 함수 사용. accumulator는 누적값, currentNumber는 현재 요소
- accumulator의 누적값에 currentNumber의 현재값을 더함
- 