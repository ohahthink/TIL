## 개발자의 마음가짐
- 원리를 이해하면 시간이 지나 잊어먹게되도 금방 다시 생각난다
- 요구사항을 명확히 한 후 > 문제분석
- 내가 작성한 코드는 말로 하나하나 짚어가며 설명할 수 있어야함
- 자바스크립트는 원리를, 꼭 원리를 알아야함


---
# for문과 while문

- While문은 무한루프를 돌아야할 때 주로 사용한다.<br>



## while문 (~하는동안 실행한다)
    • 초기화문을 먼저 선언한다
	• while문안에 증감문이 없으면 무한루프된다
	• break(=어떠한 조건을 충족했을 때 코드블럭을빠져나간다)

## Do while문
	• 일단 한번 실행하고 루프에 들어감

## Continue
	• 자신 밑에 있는 로직을 실행하지 말고 건너 뛰어라~
     (다음 구문을 실행하지 않고 다시 조건문으로 돌아가라)
	• while과 같이 사용하는 경우가 많기 때문에 꼭 외워야할 것



# 평가

	• 조건문(i < 5)을 평가하는 것
      ex) i가 5이하인지 평가하는 것
	• Truthy / Falsy value를 따져서 평가
      (트루 또는 폴스로 평가해야되는 문맥이다)

# 암묵적 형 변환

	• 형 변환이 일어나는 상황은 피해야 하는 행위이다
	• 피해갈 수 없으면 명시적으로 알려줘야한다
      (=면밀하게 처리를 해줘야 좋은 것)
	• 취향대로 쓰면 된다
      (하지만 가독성이좋다 생각되는 걸 골라 사용 하는 것을 지향)
	• +val; 이 편하고 가독성이 좋다
      (string을 number로 변환할때)
##### *빈문자열은 F / 빈객체는 T



# Checking equality

	• == / ===의 차이는 꼭 알고 있어야함
	• 요소를 취득했을때, 실패했을때 둘다 써야함
	• 삼항연산자는 한 줄로 표현가능할 때 적절히 사용하는 것을 지향


# 객체란?

> 할당할 수 있는 것을 값이라고함,<br>
즉 할당할 수 없는 것은 값이라고 하지 않는다.

**함수 = 객체에 포함되어있지 않은 것**

	• 데이터(값)와 로직(움직임)이 한 집안에 있음 > 행위를
      가지고 있음 = 프로퍼티와 메소드를 가지고 있는 것
	• 키 = 데이터를 가져오기 위한 하나의 단서 
	• 이름 = 단순 식별하기 위한 것
	• 함수도 객체이며, 값이다, 일급객체이다
	• 프로퍼티 이름과, 값으로 구성된다

## 프로퍼티

- 변수 > 첫문자에 영문 대소문자, 언더스코어 _, $ 
- 객체 > 빈 문자열을 포함하는 문자열과 숫자 
- 객체리터럴은 프로퍼티가 0개 이상 있을 수 있다 = 0포함
- 값 = 모든 값

---


# 객체 생성방식 3가지 [암기]

객체 : 기본자료형이 아닌 값들을 가르킬 때<br>
인스턴스 : 메모리상에 올라가 있는 객체의 실체 

## 객체리터럴에 의한 객체 생성방식
- 리터럴 = 값이 될 수 있는 값 자체를 가리키는 말<br>
ex) 함수는 값이 될 수 있다 > 함수 리터럴
(타언어에서는 함수가 값이 될 수 없으므로 위같은말은없다)

- 객체리터럴 = 객체를 값으로 부를 때를 말함<br>
ex) 붕어빵기계에서 틀 역할을 하는게 클래스
붕어빵은 인스턴스
(클래스는 인스턴스를 생성하기위해 존재한다)

- 표현식만으로 클래스처럼(클래스가없어도) 생성할 수 있다
- 가장 일반적이고, 많이 쓰는 방식


## 오브젝트 생성자에 의한 객체 생성방식
 
빈 객체를 만든 후 
프로퍼티가 없는데 어떤 값을 할당하면,<br>
없었던 프로퍼티(없는 프로퍼티에 값을 할당했으니까)가 생성됨<br>
**즉 프로퍼티는 나중에 추가 될 수 있는 것 = 동적 프로퍼티 할당 !**


## 생성자 함수에의한 객체 생성방식

- Function Person(name, gender) 에서 Person의 첫문자가 대문자인 이유는 기본함수가아니라 생성자함수이기 때문 

- This = Person이 만들 인스턴스를 가르킨다

- 생성자함수 = 유사한 구조의 인스턴스들을 다량으로 필요로 할 때 사용한다 / 객체를 생성하는 함수다 > 그래서 생성자 함수다 


# 객체 프로퍼티 접근

- 숫자로 만들어도 문자열로 변환된다 > 결국 프로퍼티 이름은<br>
‘문자열’이다
- 문자열이지만 프로퍼티 이름은 따옴표를 생략할 수 있다

## 프로퍼티 동적 생성

	• 없는 프로퍼티에 값을 할당하면 새 프로퍼티를 추가하고
      값도 할당하는 것

## 프로퍼티 삭제 

	• 객체를 지울 일은 없다 (우리는 최대로 null값을 만들어준다,
      그럼 가비지콜렉터가 알아서 처리)

--- 

# Pass-by-reference <-오늘의 핵심

> Runtime = 코드가 돌 때
- 힙 영역<- 동적으로 메모리를 늘었다 줄었다 할 수 있는 영역<br>
- 오브젝트는 데이터영역의 크기를 코드가 돌 때 알 수 있다.
- 주소는 바이트수가 정해져있음
- 객체의 주소를 할당함 ex)var bar = foo;
- 메모리상의 똑같은 실체를 공유하고 있는 상태가 된다 = 참조를 공유한다


# pass-by-value
- 값을 준다
- 어떻게 ? 카피해서 준다
- 그래서 ? 값을 변경해도 똑같이 변경되지 않는다
- 왜? 재할당을 하고 같은 값을 집어넣은 것뿐이지,같은실체를 참조하는 것이 아니기 때문이다 

    ___레퍼런스와, 벨류의 차이를 설명할 수 있어야한다___<br>
    ___뮤터블과 이뮤터블의 차이를 설명할 수 있어야한다___


---



# 함수 <- 굉장히 중요

- 재사용이 중점
- 언제쓸지 모르지만 재사용된다라는 확신이 있으면 정의해 놓는다, 해놓고 필요할 때 호출해놓고 사용한다
- 호출을 해야 실행된다
- 객체의 행위를 지정할 때도 사용 (메소드)
- 객체를 생성할 때도 사용 (생성자 함수)
- 함수도 객체이다 (일급객체/오브젝트나라의시민권자임 ㅎㅎ)


# 함수의 생성방식 3가지 

- 함수선언식 > 가장 일반적
- 함수표현식
- Function()함수 > (엔진이 쓴다)

##### *함수몸체 = 코드블럭 = 함수바디

## 함수 선언식
	• 함수명을 생략할 수 없다


## 함수 표현식(하나의 값으로 수렴할 수 있는 식)
	• 함수명을 생략할 수 있다
	• 이름이 있으면 기명함수표현식 / 없으면 익명함수표현식
	• 일반적으로 익명함수 표현식으로 사용한다

> 선언식과 표현식 중 어떤 것을 사용해야 하는가 ?<br>
둘다 사용해도 되지만, 둘의 성격이 조금 다르다(호이스팅이 조금 다르다)



# 호이스팅

>호이스팅이란 ? 끌어올린다

__모든 선언문은 스코프의 최상단으로 옮겨진 것처럼 동작한다__<br>
(1단계와 2단계가 한꺼번에 이루어진 것이다)

# 함수 호이스팅

함수 선언식은 선두에서 호출할 수 있다,<br>
(선언 하지도 않았는데, 호출을 할 수 있다 이상하지 않은가..?) 

- 함수선언식 = 된다 (선언이전에 호출하면 된다/undefind상태)
- 함수표현식 = 안된다 (선언이전에 호출하면 안된다)




# 변수 호이스팅

### 선언 이전에 참조하면 
>모든 변수들을 참조할 수 있다<br>
참조값을 undefind(메모리에 자리잡고 있다는 의미)<br>
이런 과정들을 호이스팅이라고 한다


#### 따라서 선언문 이전에 호출하지 않도록 하자 !!!

# ️️일급객체☝️
#### < *이거 모르면 코딩안됨 굉장히 중요한 이론 >

- 함수가 왜 값이냐? 에 관한 답
- 문법에서 지원 하는 것
- 이름이 없는 리터럴 = 무명 리터럴 
- 변수에 함수를 담을 수 있음
<!-- 
> closer 
___자바스크립트 16번 섹션 기술부채로 남겨놓을 것___ 이런게 있다 ~ 정도는 알아 먹어야되,, 말은 알아듣고 가야되,,,꼭이야...!! -->


# etc

- 변수명을 지을 때 (케밥케이스(first-name)X /  스네이크케이스(first_name)O/ 카멜케이스(firstName)O/파스칼케이스(FirstName)O
[우리가 쓸 코딩스타일은 카멜케이스]
- . 찍는 것을 = 마침표 표기법이라고함<br>
(ex. person.first-name) - 대부분 이 것을 사용합니다
- [] = 대괄호표기법<br>
(ex. Person[first-name]X        person[‘first-name’])O
- 선언식이 가독성이 좋다 
- 선언문 이전에 호출하지 않는다 
- 갈수록 난해하고 복잡해지는 코드들을 잘 독해하려면 문법을 반드시 잘 공부하고 알아두어야 한다.

# 용어정리
- 지역변수 = 코드블럭안에서만 참조할 수 있는 것<br>
- 전역변수 = 코드블럭 외에서도 참조 가능 한 것<br>
(어플리케이션이 종료되기 전까지 계속 메모리를 확보하고있는 상태)
- 객체 = 기본자료형이 아닌 값들을 가르킬 때
- 인스턴스 = 메모리상에 올라가 있는 객체의 실체 
- Runtime = 코드가 돌 때
- 함수몸체 = 코드블럭 = 함수바디
- SyntaxError = 문법에러