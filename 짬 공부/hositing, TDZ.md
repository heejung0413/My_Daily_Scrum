

1. **TDZ**(Temporal Dead Zone)란?
	1. 스코프의 시작지점부터 초기화 시작 지점까지의 구간
	2. TDZ의 3단계
		1. 1단계: 선언
		2. 2단계: 초기화 - 메모리를 만드는 단계, 할당된 메모리에는 undefined로 초기화
		3. 3단계: 할당 - 초기화된 메모리의 다른 값을 할당

## var
1. 변수 선언 전에 선언단계와 초기화단계가 동시에
*2<mark style="background: #FFB8EBA6;">. 그래서 변수 선언 전에 호출하면 undefined로 호출*</mark>

## let
1. 선언 단계와 초기화 단계가 분리되어 진행
*2.<mark style="background: #FFB8EBA6;"> 변수는 등록했지만 메모리가 할당된 값이 없어 참조 에러(ReferenceError)가 발생</mark>

