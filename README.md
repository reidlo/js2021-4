# 강준모 [201840103]

## [04월 13일]
> [7주차 04/12] 배운 내용 요약 <br>
1. 함수 생성 방법  - 함수도 하나의 자료형 취급
- 익명 함수 - 이름을 붙이지 않고 함수 생성
※ let <함수 이름(변수)> = function () {}
- 선언적 함수 - 이름을 붙여 함수 생성
※ function <함수 이름> () {}
- 화살표 함수[ECMAScript6] -'하나의 표현식을 리턴하는 함수'를 만들 시 중괄호 생략 가능
※ let 함수 = () => {}
2. 함수의 기본 형태 - 동일한 연산/판단을 써야할 시 사용
※ function <함수 이름><매개 변수> {<함수 코드> , return <리턴 값>}
- 매개 변수가 여러 개인 함수
- 리턴 없는 함수
3. 함수의 기본 활용 형태
- 리턴 하는 함수의 기본 형태
※ function (<매개변수>, <매개변수>) {let output = <초깃값>; return output;}
## [04월 06일]
> [6주차 04/06] 배운 내용 요약 <br>
1. for 반복문 복습
2. 역 for 반복문(공식명칭X) - 배열의 요소를 뒤쪽부터 출력
3. for in / for of 반복문 - 객체에 쉽게 반복문 적용 가능
※ for in - index값이 필요할 때 사용, for of - index값이 불필요할 때 사용
4. break 키워드 - 무한반복문의 강제 종료
5. 배열의 method - 데이터를 처리할 때 가장 넓게 사용되는 데이터 타입인 배열을 조작하는 방법.
- pop : 배열의 마지막 주소에 있는 값을 제거.
- shift : 배열의 첫번째 주소에 있는 값을 제거 후 반환.
- unshift : 배열의 첫번째 자리에 새로운 요소 추가 후 변경된 배열의 길이를 반환.
- push : 배열의 마지막에 새로운 요소를 추가 후 변경된 배열의 길이를 반환
- concat : 두개의 배열을 합쳐주는 함수.
- reverse : 배열을 역순으로 재배치.
- splice : 배열의 특정 위치에 배열 요소를 추가하거나 삭제.
- sort : 배열을 정렬.
- join : 배열의 모든 요소를 연결해 하나의 문자열로 만듬.
6. continue 키워드 - 반복문 내부에서 현재 반복을 멈추고 다음 반복을 진행함.
7. scope - 변수를 사용할 수 있는 범위(스코프==블록)
8. Hoisting - 해당 블록에서 사용할 변수를 미리 정리하는 키워드
## [03월 30일]
> [5주차 03/30] 배운 내용 요약 <br>
1. if / else if 조건문 - 중복되지 않은 2~3개 이상의 조건을 구분할 시 사용
2. switch case 조건문 - 비교할 값이 명확할 시 사용<br>
※ case가 끝날때 마다 break로 종료 / switch에 없는 값 입력시 default값 출력
3. 삼항 연산자 - <조건> ? <참> : <거짓>
4. 짧은 초기화 조건문 - '||' 연산자를 불이 아닌 자료에 사용할 경우<br>
※ A || B에서 A가 참이라면 A로 대치 / A || B에서 B가 참이라면 B로 대치
5. eval 함수 - 입력값을 받고 저장하는 함수 / callback함수 - 무한반복 시키는 함수
6. 반복문  - for / while / do while<br>
※ for - 반복횟수가 명확할 때 사용, while - 반복횟수가 불명확할 때 사용
7. 배열 - 여러 개의 자료를 한꺼번에 다룰 수 있는 자료형<br>
※ let 이름 = [자료,자료,자료,자료] - 배열에는 여러 자료형이 섞여 있을 수 있음
---
## [03월 23일]
> [4주차 03/23] 배운 내용 요약 <br>
1. 문자 선택 연산자
2. 템플릿 문자열(Backtit 사용)
3. 참과 거짓의 표현 / 비교 연산자, 논리 연산자
4. 변수(let)
5. 복합 대입 연산자
6. 증감 연산자
7. 자료형 검사(typeof) / Undefined 자료형
8. 강제 자료형 변환(Boolean() 함수(0, nan, "", null, undefined)
9. 자동 자료형 변환
10. 일치 연산자(자료형 검사 포함)
11. 상수(const) - '항상 같은 수'(변수의 반대)
12. if 조건문 / if else 조건문 / 중첩 조건문
---
## [03월 16일]
> [3주차 03/16] 배운 내용 요약 <br>
1. 자바스크립트의 개요
2. node.js 설치
3. javascript프로그램 실행 방법
4. REPL사용법(터미널과 크롬)
5. push 명령
---

<!-- 최근 날짜가 상위로>