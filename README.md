# 자바스크립트정리

검색어 = @\`검색어\`
ctrl + f 로 검색시 @검색어로 찾을수있게 기록

<hr>

## 프로그래밍이란

@`프로그래밍` = 프로그램을 만드는작업 <br>
@`프로그램` = 명령어모음 <br>
@`프로그래밍언어` = 컴퓨터에게 명령하는 언어, 소프트웨어를 만들기위한도구 <br>
@`명령어` = 기계어로구성 <br>
@`기계어` = 0과1로 구성, 이진법사용 <br>
@`컴퓨터` = 하드웨어 + 소프트웨어 <br>
@`하드웨어` = 기계 (컴퓨터,핸드폰) <br>
@`소프트웨어` = 여러프로그램 (윈도우,앱) <br>
@`저급언어` = 기계어에 가까운 형태, 사람이 이해하기 힘든 형태 <br>
@`고급언어` = 자연어에 가까운 형태, 사람이 이해하기 쉬운 형태 <br>
@`코드` = 컴퓨터가 알아듣는 언어 <br>
@`코딩` = 코드+ing 컴퓨터에게 코드로 명령하는것 <br>
<hr>

## 라이브러리와 프레임워크

@`Framework` = Frame(틀) + work(일) = 일정한형태의 틀로 다양한 형태의 일을하는것 = spring , django , ANGULARJS, nodejs , Flask <br>
@`Library` = 특정기능에대한도구, 함수의 집합 = 소프트웨어를 개발하기쉽게 기능을제공하는 도구 <br>

라이브러리와 프레임워크의 공통점 = 프로그램을 쉽게 만들수있게 도와줌 <br>
라이브러리와 프레임워크의 차이 = 프레임워크는 지켜야하는 규약있음, 라이브러리는 쓰던안쓰던 상관없음(자유도높음) <br>
<hr>

## 컴파일과 인터프리터

@`컴파일` = 컴퓨터로 실행 가능한 코드로 해석하는것  <br> 
@`컴파일러` = 컴파일뒤 실행파일을 생성하는 프로그램/ ex) c , c++ , pascal <br> 
컴파일을 마친 실행파일은 빠르게 실행됨, 컴파일후 생성된 코드 최적화 <br>
OS(Window, Mac)에 의존적 , 코드 변경 시 재 컴파일 필요 <br>

@`인터프리터` = 컴파일뒤 실행하는 프로그램 / 컴파일후 동시에 프로그램을 한 줄 단위로 즉시 실행시키는 프로그램/ ex) js , python , php <br>
실행파일을 생성하지않음 즉 기계어로 변환하지않음 한줄단위로 즉시 실행하기때문에 에러가 발생하면 <br> 
그즉시 중단되어 에러가 발생한부분을 찾기 쉬움
<hr>

## javascript 특징

1. 서버가 아니라 클라이언트에서 실행됨 <br>
2. 인터프리터 방식 <br>
3. 지나치게 유연함 <br>
4. script태그를 사용하여 함수정의 <br>

<hr>

## 데이터와 변수

@`데이터` = 자료 <br>
@`데이터 타입` = 공간에 저장되는 값의 종류 = 정수(음수,양수)타입 , 실수(소수점)타입 , 문자(영어,한글,특수문자...)타입 등 <br>
@`변수` = 분류된 데이터를 담을수있는 이름을가진 공간 <br>
@`할당` = 공간에 데이터를 넣는것 <br>

선언방식 = 데이터종류+변수이름+세미콜론 <br>
변수종류 = var(가변형 변수) , let(가변형 블록 지역변수) , const(불변형 블록 지역변수) <br>

+여기에 차후 let var, 호이스팅,스코프 꼬리에 연결하면 좋을거같다 <br>

<hr>

## 값(Value)와 참조(Reference)

### 값의 종류 <br>
@`원시값(Primitives)` = 단순값 , 더이상 단순화 할수없는값 = 문자 , 숫자 , 불리언 , undefind , Null , symbol <br>
* 문자
* 숫자

   - 정수 = 1 , 5 , 7 , -100
   - 부동소수점 실수(float) = 1.1, 100.5
   - 부동소수점 실수(double) = IEEE754 표준 부동소수점보다 더 정밀한 데이터 <br>
   
      + #### 부동소수점 연산 오차값 해결방법
        - toFixed(num) = num의 자리수까지 반올림해 String으로 반환
        - Math.round() = 반올림해주는 함수
        - 기타 라이브러리 = Big.js , BigNumber.js , Decimal.js  
        
* 불리언(Boolean) = 참 or 거짓
   - 거짓(false) = 0 , -0 , null , undefined , 빈문자열("") , NaN , false / 
   - 참(true) = false값이 아닐경우
* undefind = 빈값,없는값 = 변수선언후 값을 할당 받지않은 상태
* Null = 빈값,없는값 = 의도적으로 값이 없다는 것을 명시
* symbol 

@`원시타입이아닌값(non-primitive value)` = 객체값, 참조값 = 배열,함수,객체 <br>

### 데이터 타입종류 <br>
@`원시형(Primitive Type)` = 값에 의한 전달(call by value)이 일어나는 데이터타입 = 깊은복사 <br>
@`참조형(Reference Type)` = 참조에 의한 전달(call by reference)이 일어나는 데이터타입 = 얕은복사 <br>

### 타입변환

묵시적 = 자동변환 <br>
명시적 = 강제 형변환 <br>
* Number() = 문자 -> 숫자
* String() = 숫자,불리언 -> 문자
* Boolean() = 문자,숫자 -> 불리언
* Object() = 모든자료형 -> 객체
* parseInt() = 문자, 소수점있으면 -> 정수
* parseFloat() = 문자,소수점있으면 -> 소수

```javascript
let myAge;
myAge = 10; // 숫자타입(묵시적변환)
myAge = "10"; // 문자타입(묵시적변환)

console.log(Number(myAge)); // 문자->숫자(명시적변환)
```

### 앝은복사 와 깊은복사 <br>
@`얕은복사(Shallow Copy)` = 같은 주소를 참조하기때문에 원본이나 복사본의 값을 변경하면 모두 변경된다 <br>
@`깊은복사(Deep Copy)` = 원본과 주소가다른 복사본을 만들어 복사본에서 값을변경해도 원본의 값은 변경되지 않는다. <br>

<hr>

## 래퍼 객체

@`래퍼 객체(Wrapper Object)` = 원시타입의 메서드를 호출시 임시로 생성되었다가 사라지는 객체 = String, Number, Boolean, Symbol

과정 = 원시타입 메서드호출 -> 원시타입에 해당되는 객체를 생성 -> 메서드호출 -> 메서드종료후 객체삭제 -> 원시타입만 남음 <br>

Q. 왜 이렇게 복잡하게 임시로 생성했다가 제거하는지?  
A. 객체는 프로퍼티와 메서드활용에 있어서 유용하지만 무겁고 느리다 반대로 원시타입은 가볍고 빠르지만 기능이없다 <br>
그래서 원시타입의 가벼움을 유지하면서 객체의 기능도 활용하기위해 메서드를 호출할때만 임시로 객체로변환하는것 <br>

<hr>

## 객체

@`객체(Object)` = 물체 = 키(key)와 값(value)의 집합

### 객체프로퍼티 참조방식

@`프로퍼티(property)` = 객체가 가지고있는 속성

객체이름.프로퍼티 이름 <br>
객체이름["프로퍼티 이름"] <br>

### 객체 메소드 참조방식
객체이름.메소드 이름()

<hr>
 
## 연산자

@`연산자(operator)`  = 연산에 사용되는 기호 = +,-,* <br>
@`피연산자(operand)` = 연산의 대상 = 1, 5, 10 <br>

### 연산자종류

산술 연산자 = +(덧샘), -(뺄샘) , *(곱) , /(나누기) , %(나머지) <br>
증감 연산자 = ++(1씩증가) , --(1씩감소) / ++num , num++, --num , num-- <br>
비교 연산자 = > , >= , < , <= , == , != , === , !=== / 결과는 참 or 거짓 <br>
논리 연산자 = &&(and) , ||(or) , !(not) <br>
...등

@`식(expression)` = 연산자 + 피연산자 , 값이존재

<hr>

## 함수

@`함수(function)` = 기능 = 기능을 구현한 코드집합  <br>
사용하는이유 = 반복적인 코드작성을 피할수있음 (개발시간단축), 코드 간결화로 가독성높아짐, 쉬운유지보수  <br>
합수호출(function call) = 기능부르기 = ex) 함수이름(파라미터1...) <br>

@`파라미터(parameter)` = 매개변수 = 함수,메서드에서 입력값으로 제공되는 변수이름 <br>
```javascript
function WhatIsMean(parameter1,parameter2) {
  return parameter1 + parameter2
}
```
@`아규먼트(argument)` = 전달인자 = 함수,메서드에서 입력되는 값(Value)
```javascript
//function call 
WhatIsMean(argument1,argument2)
```

<hr>

## 문

@`문(statement)` = 어떤 것을 수행하는 구문 단위 , 함수 기능을 구현한 코드로사용

### 조건문

@`if문` <br>
@`else if문` <br>
@`else문` <br>
```javascript
if(i=0){ //i가 0일경우 로직실행
  //로직실행
}
else if(i<0){ //i가 0보다 작을경우 로직실행
  //로직실행
}
else{ //그외 다른 모든경우 (0<i) 로직실행
  //로직실행
}
```

@`switch문` <br>
```javascript
switch (대상) {
    case 조건값1: // 조건값1과 대상이 일치할경우 로직실행
        //로직실행
        break; // 생략가능
    case 조건값2: // 조건값2과 대상이 일치할경우 로직실행
        //로직실행
        break; // 생략가능
    default: // 생략가능 조건값1,2에 해당사항이없을경우
        //로직실행
}
```

### 반복문

@`for문` 
```javascript
//i가 3보다작으면 실행후 i값 +1후 반복
for(let i=0; i<3; i++;){ //(초기화; 조건식; 증감식)
  //로직실행
}
```
@`while문` 
```javascript
//i가 3보다작으면 실행후 i값 +1후 반복
let=0; 
while(i<3){ 
  //로직실행 
  i++
}
```

@`do while문` 
```javascript
// 조건확인없이 1번실행후 조건확인
let i = 1; 
do { 
//로직실행    
i++
} while(i < 3);
```

<hr>

## 숫자 

@`상수(constant)` = 코드에서 변하지 않는 변수(메모리 위치)
@`리터럴(literal)` = 코드에서 변하지 않는 데이터(메모리위치 안의 값)

### 숫자 리터럴

- 정수 리터럴
   * 10진수 또는 16진수
   * 10진수 -> 0 ~ 9
   * 16진수 -> 0xFF , 0x12 , 0x1F (0~9 , 10~15 -> A~F)

- 부동 소수점
   * 실수표기 -> 10.1 , 11.1 , 0.11
   * 지수표기 -> 2e2 , 2e-2
   
- Infinity(무한) = 무한대를 나타내는 숫자값
- NaN(Not a Number) = 숫자가 아님을 나타내는 값
- 특수값

### BigInt
BigInt = Number의 최대값보다 큰 정수표현
* Math 객체의 메서드와 함께 사용불가
* 연산에서 Number와 함께 사용불가

BigInt연산
* +,*,-,**,%를 이용해서 연산가능
* BigInt 객체를 이용

<hr>

## 문자열

문자열 = 텍스트 형식의 데이터 / 부호없는 정수 값의 요소 집합 / 큰따옴표 , 작은따옴표 , 백틱으로 표현 <br>

특수문자 <br>
* |n = 다음 줄로 이동
* |t = 탭(4칸)만큼 이동
* || = 문자표시
* |" = 큰따옴표 표현
* |' = 작은따옴표 표현

### 문자열 접근

charAt() = 문자접근 <br>
```javascript
let text = "Hello";
text.charAt(num)
//num번째 문자접근, 반환값은 num번째 문자

```
charCodeAt() <br>

startsWith() = 특정문자로 시작하는지 확인 <br>
```javascript
let text = "Hello";
text.startsWith(searchStr);
text.startsWith(searchStr,position);
// searchStar = 탐색할문자열 
// position = 탐색시작할 위치
// 반환값 = true or false
```
endsWith() = 특정문자로 끝나는지 확인 <br>
```javascript
let text = "Hello";
text.endsWith(searchStr);
text.endsWith(searchStr,position);
// searchStar = 탐색할문자열 
// position = 탐색시작할 위치
// 반환값 = true or false
```

indexOf() = 문자열 검색<br>
```javascript
let text = "Hello";
text.indexOf(searchStr);
// searchStr = 탐색할 문자열
// 반환값 = index
// 일치하지않을경우 -1반환
```

lastIndexOf() <br>

문자열[index] = 문자열접근 <br>
```javascript
let text = "Hello"
text[0]; // "H"
text[4]; // "O"
// 해당 문자열 인덱스에 위치한 문자반환
```

더하기연산
replace()
replaceAll()
toLocaleLowerCase()
toLocaleUpperCase()
toLowerCase()
toUpperCase()

<hr>

### 변환,확인

@`변환`
Number.parseInt(num) = 정수로 변환하는 함수 / 반환타입은 Number <br>
Number.parseFloat(num) = 실수로 변환하는 함수 / 반환타입은 Number <br>

@`확인`
Number.isInteger(num) = 정수인지 판별하는 함수 / 반환값은 Boolean(true, false) <br>
Number.isNaN(num) = NaN인지 판별하는 함수 / 반환값은 Boolean(true, false) <br>

<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>

<hr>

<hr>

## 알고리즘 

### 시간 복잡도

O(빅오) = 최악의 상황을 고려하여 성능 측정 결과표현 <br>
θ(세타) = 평균적인 경우에서의 성능 측정 결과 표현 <br>
Ω(오메가) = 최선의 상황일 때의 성능 측정 결과 표현 <br>

<hr>

## VScode 단축키

@`단축키모음`

행삭제 = Ctrl + X <br>
복사 = Ctrl + C <br>
아래 빈 줄 생성 = Ctrl + Enter <br>
위 빈 줄 생성 = Ctrl + Shift + Enter <br>
행 위로 이동 = Alt + ↑ <br>
행 아래로 이동 = Alt + ↓ <br>
다중선택으로 커서를 위에 추가 = Ctrl + Alt + ↑ <br>
다중선택으로 커서를 아래에 추가 = Ctrl + Alt + ↓ <br>
주석처리 = Ctrl + / <br>
선택부분 주석처리 = Alt + Shift + A <br>
라인 번호 찾기 = Ctrl + G <br>
프로젝트 내에서 파일 찾기 = Ctrl + P <br>
문자열 찾아 수정 = Ctrl + H <br>
프로젝트 전체 페이지 문자열 수정 = Ctrl + Shift + H <br>
새파일 열기 = Ctrl + N <br>
현재 파일 창닫기 = Ctrl + W  <br>
이전에 닫힌파일 다시열기 = Ctrl + Shift + T <br>
전체선택 = Ctrl + A <br> 
자동 정렬 = Ctrl + A - Ctrl + K - Ctrl + F <br>
프로젝트 전체 페이지 문자열 수정 = Ctrl + Shift + H <br>
<hr>
