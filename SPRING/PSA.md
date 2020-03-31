# PSA

## Portable Service Abstraction
 - [Service Abstraction](https://en.wikipedia.org/wiki/Service_abstraction)
 - Portable: 내 코드를 둔 상태로 다른 기술 스택으로 전환 가능

## Spring 이 제공하는 Service Abstraction

### Spring Web MVC
 - @Controller | @ReuqestMapping | ..
 - Servlet | Reactive
 - 톰캣, 제티, 네티, 언더토우

### Spring Transaction Manager
 - @Transactional
 - PlatformTransactionManager
 - JpaTransacionManager | DatasourceTransactionManager | HibernateTransactionManager

### Spring Cache
 - @Cacheable | @CacheEvict | ...
 - CacheManager
 - JCacheManager | ConcurrentMapCacheManager | EhCacheCacheManager | ...

## Comment
 * [예제로 배우는 스프링 입문. 백기선님. 인프런](https://www.inflearn.com/course/spring_revised_edition/dashboard)