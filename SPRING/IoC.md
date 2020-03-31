# IoC(Inversion of Control)

## 역전된 제어

> 역전 (逆轉) [명사]
> 1. <b>형세가 뒤집힘. 또는 형세를 뒤집음.</b>
> 2. 거꾸로 회전함.
> 3. 일이 잘못되어 좋지 아니하게 벌어져 감.

 - 역전의 사전적 정의다.
 - 간단한 예시를 통해 보는 IoC

```java
// 일반적인 사용 예시. 사용자가 의존성을 직접 관리
class OwnerController {
    private Owner Repository repository = new OwnerRepository();
}
```
```java
/**
  * 내가 사용할 의존성을 누군가 알아서 해주겠지.
  */

class OwnerController {
    private OwnerRepository repo;

    public OwnerController(OwnerRepository repo) {
        this.repo = repo;
    }
}
```

## IoC Container
### Application Context (BeanFactory)
 - bean 을 만들어주고, 연결해주면서, 제공해준다.
 - bean 설정
    - 이름 또는 ID
    - 타입
    - 스코프

## Bean
 - 스프링 IoC 컨테이너가 관리하는 객체
 - How to Register
    - Component Scanning
        - @Repository
        - @Service
        - @Controller
        - @Configuration
    - 또는 사용자 정의 (XML 혹은 자바 설정파일에 등록)
 - How to Use
    - @Autowired 또는 @Inject
    - ApplicationContext 의 getBean()을 이용

## 의존성 주입(Dependency Injection)
> As a result I think we need a more specific name for this pattern. Inversion of Control is too generic a term, and thus people find it confusing. As a result with a lot of discussion with various IoC advocates we settled on the name Dependency Injection.
>결과적으로 나는 우리가 이 패턴을 위해 더 구체적인 이름이 필요하다고 생각한다. 제어의 역전은 너무 일반적인 용어여서 사람들은 그것을 혼란스럽게 생각한다. 그 결과 다양한 IoC 옹호자들과의 많은 토론으로 우리는 Dependency Injection이라는 명칭을 정했다.

## Comment
 * [예제로 배우는 스프링 입문. 백기선님. 인프런](https://www.inflearn.com/course/spring_revised_edition/dashboard)
 * [Inversion of Control Containers and the Dependency Injection pattern. 마틴 파울러](https://martinfowler.com/articles/injection.html)