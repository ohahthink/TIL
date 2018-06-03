# Pass-by-value VS Pass-by-reference
- pass by value : 값을 참조하는 것<br> steck영역의 메모리에 할당된 값을 복사하여 다른 위치(주소)에 재할당한 후 참조하게된다<br>

- pass by reference : 위치(주소)를 참조하는 것<br> 스택영역과 달리 
메모리가 늘었다 줄었다가 가능한 동적인 힙영역의 메모리에 할당된 값을, 스택영역 메모리의 값에 할당된 힙영역의 주소(위치)로부터 참조하게된다

#  Object의 property VS method
- property : 객체(Object)의 데이터, 키(이름)와 키벨류(값)을<br>가지고 있다
- method : 객체의 동작, 객체의 property가 함수인 경우

# Hoisting
- 선언문이 스코프의 최상단에 있는 것처럼 동작하는 현상
- 선언이전에 참조 할 수 있는 현상이 발생한다(ex.선언하지도 않았는데 호출이 가능한 기이한 현상)
- 변수 호이스팅과 함수 호이스팅의 차이