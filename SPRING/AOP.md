# AOP 

## Aspect Oriented Programming

 - 기존 비즈니스 로직을 건드리지 않고, 공통적인 부분을 처리
```java
class A {
   method a () {
           AAAA -> AAA
           오늘은 7월 4일 미국 독립 기념일이래요.
           BBBB -> BB
   }
 
   method b () {
           AAAA -> AAA
           저는 아침에 운동을 다녀와서 밥먹고 빨래를 했습니다.
           BBBB -> BB
   }
}

class B {
  method c() {
          AAAA -> AAA
          점심은 이거 찍느라 못먹었는데 저녁엔 제육볶음을 먹고 싶네요.
          BBBB -> BB
  }
}
```
```java
// 모아 놓은 AAAA 와 BBBB

class A {
   method a () {
           오늘은 7월 4일 미국 독립 기념일이래요.
   }
 
   method b () {
           저는 아침에 운동을 다녀와서 밥먹고 빨래를 했습니다.
   }
}

class B {
  method c() {
          점심은 이거 찍느라 못먹었는데 저녁엔 제육볶음을 먹고 싶네요.
  }
}

class AAAABBBB {
    method aaaabbb(JoinPoint point) {
         AAAA
	  point.execute()
         BBBB
    }
}

```
## AOP 구현방법
 - AspectJ
    - compile <b>e.g.</b> A.java ---(AOP)---> A.class
    - 바이트 코드 조작 <b>e.g.</b> A.java -> A.class ---(AOP)---> 메모리 
    - proxy pattern
 - 캐시, 트랜잭션 처리 등 활용 가능

 ## Comment
 - [예제로 배우는 스프링 입문. 백기선님. 인프런](https://www.inflearn.com/course/spring_revised_edition/dashboard)