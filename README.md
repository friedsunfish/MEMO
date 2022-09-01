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

@`연산자(operator)` = 연산에 사용되는 기호 (= +,-,*) <br>
@`피연산자(operand)` = 연산의 대상 (1, 5, 10) <br>
@`식(expression)` = 연산자 + 피연산자 , 값이존재

### 기본연산자 (+, -, *, **, /, %)
* 산술연산자 = 변수또는 값을 산술하기 위한 연산자 <br>
   - +10 //result = 양수10 <br>
   - -10 //result = 음수10 <br>
   - 10+2 //result = 12 <br>
   - 10-2 //result = 8 <br>
   - 10*2 //result = 20 <br>
   - 2**3 //result = 8 <br>
   - 10/2 //result = 5 <br>
   - 10%2 //result = 0 <br>

* 증감연산자 (++,--)
   - 전위 증감 연산자 (값반환 전 증감)
      - ++num 
      - --num
   - 후위 증감 연산자 (값반환 후 증감)
      - num++
      - num-- <br>
      
ex) 
```javascript
let a = 0;
let b = 0;
console.log(a++) // result = 0
console.log(++a) // result = 1
```

* 대입(할당)연산자 = 변수에 값을 할당하는 연산자
   - a=b // a=b => b를 a에 대입
   - a+=b // a=a+b => a와 b를 더한값을 a에 대입
   - a-=b // a=a-b => a에서 b를 뺀값을 a에 대입
   - a*=b // a=a*b => a와 b를 곱한값을 a에 대입
   - a/=b // a=a/b => a와 b를 나눠 나온 몫값을 a에 대입
   - a%=b // a=a%b => a와 b를 나눠 나온 나머지값을 a에 대입

### 비교연산자
* 비교 연산자
   - a > b // a가 b보다 크면 참,아니면 거짓
   - a < b // a가 b보다 작으면 참,아니면 거짓
   - a >= b // a가 b보다 크거나 같으면 참,아니면 거짓
   - a <= b // a가 b보다 작거나 같으면 참,아니면 거짓
   - a == b // a와 b가 같으면 참, 아니면 거짓
   - a === b // a와 b의 값또는 데이터타입이 같으면 참, 아니면 거짓
   - a != b // a와 b가 다르면면 참, 아니면 거짓
   - a !== b // a와 b의 값또는 데이터타입이 다르면 참, 아니면 거짓

* 삼항 조건 연산자
=> 변수 = (조건식) ? 값1:값2

```javascript
isBig = (a>=b) ? "big" : "small" // a가 b보다 크거나 같을 경우 "big" 아닐경우 "small"
```

중첩가능예시)
```javascript
let myAge = 60;
let rtn = (myAge<20) ? "청소년" : ((myAge>=20 && myAge<50) ? "어른" : ((myAge >= 50) ? "중장년" : "-"));
```

* 논리 연산자 = 참과 거짓을 이용하여 연산하는 연산자
   - a && b // a and b => a와b 모두 true면 true 하나라도 false면 false
   - a || b // a or b => a와b중 하나라도 true면 true 둘다 false면 false
   - !a // NOT a => a가 true면 false , false면 true

### 고급 연산자
* 비트연산자 = 32비트 숫자에서 작동하는 연산자
   - & (And) // a와 b둘다 1이면 1
   - | (OR) // a와 b둘중 하나가 1이면 1
   - ~ (NOT) // 비트가 1이면 0, 0이면 1로변경
   - ^ (XOR) // 두비트가 서로 다르면 1반환
   - << (Left Shift) // 비트를 왼쪽으로 이동
   - \>> (Right Shift) // 부호 유지하면서, 비트를 오른쪽으로 이동 

ex) <br>
5를 비트로 표현하는 과정 <br>
2^3=8 => 넘치기때문에 버림 = 0 <br>
2^2=4 => 5보다 작으니까 챙김 = 1 <br>
2^1=2 => 4를챙겨 1이남는데 1보다 크니까 버림 = 0 <br>
2^0=1 => 1이남고 딱맞게 챙길수있으니 챙김 =1 <br>
5 = 0101 <br>

가장앞자리 1일경우 음수 <br>
1010 = -6 <br>
2^3 = -8  <br>
2^2 = 4 <br>
2^1 = 2  <br>
2^0 = 1 <br>
=> -8+2 =-6 <br>

* typeof연산자 = 데이터타입을 반환해주는 연산자 
   - string , number , boolean , object , function , undefined

* instanceof연산자 = 어떤객체에 대하여 지정한 객체의 데이터 타입에 대한 결과를 반환하는 연산자 <br>
=> <br>
변수 instanceof Array

### 기타연산자
* 삭제 연산자 = 어떤객체가 있을때, 그객체의 값을 삭제하는 연산자
=> delete객체.객체키

* in 연산자 = 어떤 객체안에 어떤 값이 존재하는지 결과값을 반환하는 연산자 (true,false반환)
```javascript
const cars = ["Saab","Volvo","BMW"] 
 "Saab"in cars // false
0 in cars // true
```
값을찾는게아닌 key값(index)으로 찾는것

- void 연산자 = void(0)을 사용해 정의되지 않는 곳에 사용하는 연산자 <br>
=> <br>
\<a href="#">클릭\</a> <br>
\<a href="jacascirpt:void(0);">클릭\</a> <br>

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

indexOf() = 문자열 검색(처음 나오는값) <br>
```javascript
let text = "Hello";
text.indexOf(searchStr);
// searchStr = 탐색할 문자열
// 반환값 = 처음으로 등장하는 index / 없다면 -1
```

lastIndexOf() = 문자열 검색(마지막으로 나오는값) <br>
```javascript
let text = "Hello";
text.lastIndexOf(searchStr);
// searchStr = 탐색할 문자열
// 반환값 = 마지막으로 등장하는 index / 없다면 -1
```

문자열[index] = 문자열접근 <br>
```javascript
let text = "Hello"
text[0]; // "H"
text[4]; // "O"
// 해당 문자열 인덱스에 위치한 문자반환
```

### 문자열 변경

더하기연산
```javascript
let text = 123 + "" // "123" (type string)
let text2 = "안" + "녕" // "안녕" (type string)
```

replace() = 바꿀문자열 선택후 가장첫번째 문자를 변경
```javascript
let text = "Hello World"
let text2 = text.replace("l","L"); // "HeLlo World"
```

replaceAll() = 바꿀문자열 선택후 해당되는 모든 문자변경
```javascript
let text = "Hello World"
let text2 = text.replaceAll("l","L"); // "HeLLo WorLd" 
```

toLowerCase() = 모든 대문자를 소문자로 변경
```javascript
let text = "HeLlo";
text.toLowerCase(); // "hello"
```

toUpperCase() = 모든 소문자를 대문자로 변경
```javascript
let text = "HeLlo";
text.toUpperCase(); // "HELLO"
```

toLocaleLowerCase() , toLocaleUpperCase() <br>
각각 toLowerCase(), toUpperCase()와 유사하게 동작하지만 대소문자 매핑이 유니코드의 <br>
지본 대소문자 매핑을 따르지않는 터키어같은 일부 로케일에 대해서 다를수있음 <br>

### 문자열 병합

더하기연산
```javascript
let text1 = "Hello"
let text2 = "World"
let plus = text + " " + text2 // "Hello World"
```
concat() = 배열이나 값을 합쳐서 반환
```javascript
let text1 = "Hello"
let text2 = "World"
text1.concat(text2); // "HelloWorld"

let arr1 = ["H" , "e" , "l"]
let arr2 = ["l" , "o" , "w"]
arr1.concat(arr2) // H,e,l,l,o,w (type object)
arr1.concat(arr2,"2","3")
```
join() = 배열을 하나의 문자열로 합쳐서 반환
```javascript
let arr = ["H", "e", "l", "l", "o", "w"];
let str = arr.join(); // H,e,l,l,o,w
구분자 선택가능 선택안할시 기본 = ,
띄어쓰기없이 = ""
띄어쓰기 = " "
다른구분자로 구분가능
```

<hr>

## 배열
```javascript
let arr = [] // 대괄호로 배열 표현
let arr2 = ["문자" , 2] // 문자, 숫자 혼합가능
arr.length // 2 (문자열의 길이)
arr2[1] // 2 (인덱스접근)
```
### 배열생성
split() = 문자열을 구분자로 분리해서 배열로 반환
```javascript
let text = "a_b_c";
let arr = text.split("_");
console.log(arr); // [ 'a', 'b', 'c' ]
```
Array.from() = 문자들을 분리해서 배열로 반환하는함수
```javascript
let text = "abc";
let arr = Array.from(text);
console.log(arr); // [ 'a', 'b', 'c' ]
```
스프레드 연산자(...) = 문자열을 분리해서 배열로 반환하는 연산
```javascript
let text = "abc";
let arr = [...text];
console.log(arr); // [ 'a', 'b', 'c' ]
```
### 배열요소 편집
push() = 배열끝에 추가 <br>
pop() = 배열 마지막 요소 제거 <br>
unshift() = 배열 앞에 추가 <br>
shift() = 배열 첫번째요소 제거 <br>
slice() = 시작과 끝범위 요소를 잘라 새로운 배열 생성 <br>
splice() = 일정 범위요소 삭제, 새로운 요소추가 <br>
concat() = 합치는 기능 <br>
-문자열 병합참고 <br>
join() = 배열 합쳐서 문자열로 반환 , 구분자이용가능 <br>
-문자열 병합참고 <br>

### 배열검색 
indexOf() = 배열 검색후 가장첫번째 요소 위치값 반환 없으면 -1 <br>
lastIndexOf() = 배열 검색후 가장첫번째 요소 위치값 반환 없으면 -1 (역순) <br>

### 배열정렬
sort() = 배열 정렬 <br>
reverse() = 배열 거꾸로 뒤집기 <br>

<hr>

## 템플릿 리터럴(Template literals)
템플릿 리터럴 = 내장된 표현식을 허용하는 문자열 리터럴

### 개행
```javascript
let text = "hello\nWorld";
=
let text = `hello
World`;
```

### 표현식사용
```javascript
let text = "hello World";
let textType = typeof text;
console.log(`${text} 타입은 ?? ${textType}`);
```

<hr>

### 변환,확인

@`변환`
Number.parseInt(num) = 정수로 변환하는 함수 / 반환타입은 Number <br>
Number.parseFloat(num) = 실수로 변환하는 함수 / 반환타입은 Number <br>

@`확인`
Number.isInteger(num) = 정수인지 판별하는 함수 / 반환값은 Boolean(true, false) <br>
Number.isNaN(num) = NaN인지 판별하는 함수 / 반환값은 Boolean(true, false) <br>

<hr>

## 동기와 비동기
 
동기 = 동시에일어나는 = 요청과 동시에 결과가 동시에 일어남  <br>
-> 설계간단,직관적 but 결과가 주어질때까지 대기 <br>
비동기 = 동시에 일어나지않는 = 요청과 동시에 결과가 동시에 일어나지않음 <br>
-> 동기보다 복잡 but 결과가 주어지는데 시간이걸리더라도 다른작업을할수있음 효율적 <br>

커피주문후 나올때까지 줄을서서 기다림 = 동기 <br>
커피주문후 진동벨이울리면 가지러감 = 비동기 <br>

### 비동기 사용방법 3가지

Callback 함수 = 함수를 실행후 이후에 실행되는 함수, 다른함수에 파라미터로 넘겨지는 함수 <br>
```javascript
//사용예시
//함수선언
function sum(num1, num2, callback){
  var result = num1 + num2;
  callback(result);
}
//함수호출
sum(10, 20, function(result){ 
  console.log(result);
});
```

Promise = 비동기처리에 사용되는 객체 , 비동기실행결과를 반환(성공 or 실패)   <br>

pedding(대기) = 초기상태 <br>
Fullfilled(이행) = 성공 <br>
Rejected(거부) = 실패 <br>
then() = 결과값과 로직 담은것을 콜백함수로 받음 (resolve시실행)<br>
catch() = 예외처리하는 로직을 콜백함수로 받음 (reject시실행)<br>
resolve, reject = 인수를 전달하는 실행함수 <br>
resolve = 비동기 작업 종료시 resolve 호출하여 실행 <br>
reject = 비동기 작업 중간 오류 발생 시 reject호출하여 실행

```javascript
//사용예시
//함수선언
function sum(num1, num2){
  return new Promise((resolve,reject)=>{
    if(num1 == null || num2 == null) reject(new Error("num1 또는 num2 null 값"));
    else resolve(num1 + num2);
  });
}
//함수호출
sum(10,20)
  .then((result)=>console.log("성공 ::: 결과는? "+result))
  .catch((error)=> console.log("실패 ::: "+error));

```

### async / await

async / await = 비동기처리위해 사용, Promise단점보안, Callback hell해결
async = 동기
await = 기다리다
try ~ catch = 에러 발생시 핸들링

```javascript
const sum2 = async (num1, num2) => {
  const promise = new Promise((resolve, reject)=>{
    if(num1>num2) resolve(num1-num2);
    else resolve(num2 - num1);
  });
  try{
    const result = await promise;
    console.log(result);
  }catch(error){
    console.error(error);
  }
}
sum2(10,20);
```

<hr>
<hr>
<hr>
<hr>
<hr>
<hr>
<hr>

 json-server로 fake api 구축
 
 설치방법
 터미널에 npm install -g json-server
 
 실행방법
 터밀널에 json-server --watch db.json

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
