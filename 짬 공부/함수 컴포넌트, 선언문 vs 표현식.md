

```
//함수 선언문
function Fn() {}


// 함수 표현식
const fn = () => {}
```

1. 선언문과 표현식
	- 호이스팅 여부
	- export default 선언과 동시에 할 수 있는가
	1. 호이스팅
		1. 함수 선언문일 경우 함수 호이스팅이 가능해 메인 로직만 상단에 배치함으로써 가독성을 높일 수 있음
		2. 표현식일 경우 실행 로직이 없는 모듈의 경우에는 특별히 호이스팅 이슈에 걸리는 경우는 없다. 다만, TDZ는 표현식에서 항상 존재할 수 있는 이슈
	2. export default
		1. 
```
// 선언문은 함수 선언과 export default를 동시에 할 수 있다.
export default Fn(){}

// 표현식은 불가능하다
export default const Fn = () => {} // error

// named export는 가능하다
export const Fn = () => {}
```

2. React.FC 특징
	1. 함수 표현식 컴포넌트 함수의 타입으로 지정
	2. <mark style="background: #FFF3A3A6;">함수 선언식에서는 사용할 수 없음</mark>
	3. 