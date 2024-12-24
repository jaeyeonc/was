# spring-boot-sample project by ucpwang
- GitHub : https://github.com/ucpwang/spring-boot-sample

## spec
- java 1.8.x
- mvn 3.2.x
- spring-boot 1.4.x
- use lombok lib
- use `thymeleaf` view template
- use `mysql` database > jdbc
- use `logback` logger

## install && excute

### install
```bash
$ git clone git@github.com:ucpwang/spring-boot-sample.git

or

$ git clone https://github.com/ucpwang/spring-boot-sample.git
```

### run
run with `mvnw`
```bash
$ chmod 700 ./mvnw && ./mvnw spring-boot:run
```
or

use maven build and java jar excute
```bash
$ mvn clean && mvn package
$ java -jar ./target/spring-boot-sample-0.0.1-SNAPSHOT.jar
```
or

use maven > `spring-boot-maven-plugin` run
```bash
$ mvn spring-boot:run
```

## mission
- CORS
- AOP 구성
- 샘플 RESTful API 구성
  - 목록조회
  - 상세조회
  - 등록
  - 수정
  - 삭제
- 샘플로직에 대한 단위테스트 작성
- mysql datasource 적용
- favicon
- 다국어 전처리
- 로그인 > 리멤버미
  - http://blog.naver.com/PostView.nhn?blogId=wizardkyn&logNo=220663952961
- webjars-locator 적용

## Doing
- XSS 필터 적용 : https://github.com/naver/lucy-xss-filter

## Done
- spring-boot > banner 적용
- logback 설정 적용
- thymeleaf
  - 뷰리졸버 적용
- profile 설정
- properties -> yaml 적용
- spring security > 복수 admin properties 에서 읽어서 적용하기
- 로그인 페이지 UI 적용
  - 참고 : http://codepen.io/DamirZ/pen/dYpoZY
- interceptor 구성
  - BasicInterceptor 적용
- frount-end lib 적용
    - webjars 적용
      - http://www.webjars.org/documentation#springboot
      - http://adrenal.tistory.com/14
      - 자동 설정에 webjars 관련 설정하는 부분을 확인할 수 있음 -> 고로 별도 설정하지 않아도 됨
        - org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter.addResourceHandlers
- spring security 기본 적용
- thymeleaf
  - layout 적용 > @Layout 어노테이션 인터셉트 방식 적용 (http://blog.codeleak.pl/2013/11/thymeleaf-template-layouts-in-spring.html)
- error 페이지에 대한 전처리 적용

## note
- junit4 단위 테스트 
  - controller 테스트케이스 작성중 spring-boot 1.4로 넘어오면서 `@SpringApplicationConfiguration`가 Deprecated 됨을 인지
    - 참고 : https://spring.io/blog/2016/04/15/testing-improvements-in-spring-boot-1-4
    - `@SpringBootTest` 사용으로 훨씬 심플해진 느낌아닌 느낌 :)
- `thymeleaf-layout-dialect` 미적용

## etc
- spring-boot reference : http://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/
- http://jsonobject.tistory.com/219
- Spring boot devTools 관련 : http://blog.sbcoba.com/30
- properties 관련 : http://docs.spring.io/spring-boot/docs/current/reference/html/common-application-properties.html
- Spring에서 YAML 파일 데이터 객체에 매핑하여 로드하기 : http://blog.saltfactory.net/java/load-yaml-file-in-spring.html
- spring-boot tomcat 연동 관련 : http://blog.woniper.net/231
- spring > Securing a Web Application : https://spring.io/guides/gs/securing-web
- spring > security 관련 : http://www.namooz.com/2015/12/07/spring-boot-thymeleaf-10-spring-boot-security-final
- spring-boot > ConfigurationProperties : http://docs.spring.io/spring-boot/docs/1.4.0.RELEASE/reference/html/configuration-metadata.html#configuration-metadata-annotation-processor
- Spring MVC Matrix Variables : http://www.baeldung.com/spring-mvc-matrix-variables
- howto-reload-java-classes-without-restarting : http://docs.spring.io/spring-boot/docs/current/reference/html/howto-hotswapping.html#howto-reload-java-classes-without-restarting
- spring exception handling 관련 : https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc
- spring-boot using thymeleaf : https://springframework.guru/spring-boot-web-application-part-2-using-thymeleaf
  - thymeleaf guide : http://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#a-multi-language-welcome
  - thymeleaf > layout
    - default examples : https://github.com/thymeleaf/thymeleafexamples-layouts
    - https://blog.outsider.ne.kr/1004
    - https://github.com/ultraq/thymeleaf-layout-dialect / https://ultraq.github.io/thymeleaf-layout-dialect