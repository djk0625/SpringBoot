# Spring Boot

## 인프런 김영한 강사님의 스프링 입문 - 코드로 배우는 스프링 부트, 웹 MVC, DB 접근 기술 강의

<p>강의 주소 : <a href="https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%EC%9E%85%EB%AC%B8-%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8">[스프링 입문 강의]</a></p>

예제 코드를 따라해보면서, 실습하였습니다.

### 웹 개발 방식

* 정적 컨텐츠 : 파일을 그대로 웹 브라우저에 내려주는 방식
<img src="C:\Users\ko\Desktop\Spring\정적 컨텐츠.png" width = "450px" height = "300px"></img><br/>

* MVC와 템플릿 엔진 : Model, View, Controller로 나눈 후, 서버에서 html을 동적으로 프로그래밍하여 내려주는 방식
<img src="C:\Users\ko\Desktop\Spring\MVC.png" width = "450px" height = "300px"></img><br/>

* API : JSON이라는 데이터 구조 포맷으로 클라이언트에게 데이터를 전달하는 방식
<img src="C:\Users\ko\Desktop\Spring\API.png" width = "450px" height = "300px"></img><br/>

### TDD (Test-Driven Development)

* 테스트 주도 개발이라는 의미로, 작은 단위의 테스트 케이스를 작성하고, 이를 통과하는 코드를 추가하는 단계를 반복하여 소프트웨어를 구현하는 방법

- 장점
1) 클린 코드를 위한 확신 : 잘 정의된 테스트 케이스가 존재할 경우, 코드 수정 이후에도 즉각적인 테스트가 가능
2) 높은 소스 코드 품질
3) 재설계 시간과 디버깅 시간 절감

- 단점
1) 생산성 저하
2) 러닝 커브
3) 초기 개발 비용 증가

### 스프링 빈을 등록하는 2가지 방법
1) 컴포넌트 스캔과 자동 의존관계 설정 : @Component 애노테이션이 있으면 스프링 빈에 자동 등록
* @Component를 포함하는 @Controller, @Service, @Repository 와 같은 애노테이션도 스프링 빈으로 자동 등록된다.

2) 자바 코드로 직접 스프링 빈 등록
* @Service, @Repository 와 같은 애노테이션을 제거하고, @Bean 을 이용하여 직접 설정 파일을 이용하여 등록

### DI (Dependency Injection)
* 의존성 주입이라고 하며, 필드 주입, setter 주입, 생성자 주입 3가지 방법이 있다.
* setter 주입은 항상 public으로 열려 있어서, 아무나 호출이 가능하다.
* 의존 관계가 동적으로 변하는 경우가 거의 없기 때문에, 생성자 주입을 권장한다.