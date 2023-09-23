# SPRING

### \[Q\] Spring Framework란?

\[A\]  
스프링 프레임워크는 자바 개발을 편리하게 해주는 오픈소스 프레임워크 입니다.  
Spring Framework의 첫번째 특징은 경량 컨테이너로서 객체 생성, 소멸과 같은 라이프 사이클을 관리하며 스프링으로부터 필요한 객체를 얻어올 수 있습니다.  
두번째 특징은 컨트롤의 제어권이 사용자가 아닌 프레임워크에 있어 필요에 따라 스프링에서 사용자의 코드를 호출는 제어의 역전(IoC)을 통해 어플리케이션의 결합도를 낮춥니다.  
세번째 특징은 의존성 주입(DI, Dependency Injection)을 지원하여 각각의 계층이나 서비스들 간에 의존성이 존재할 경우 프레임워크가 서로 연결시켜줍니다.  
마지막으로 관점 지향 프로그래밍(AOP, Aspect-Oriented Programming)으로 트랜잭션이나 로깅, 보안과 같이 여러 모듈에서 공통적으로 사용하는 기능의 경우 해당 기능을 분리하여 관리할 수 있습니다.

<br>

### \[Q\] 라이브러리 vs 프레임워크

\[A\]  
프레임워크는 원하는 기능 구현에 집중하여 개발할 수 있도록 일정한 형태와 필요한 기능을 갖추고 있는 골격, 뼈대를 의미합니다.  
애플리케이션 개발 시 필수적인 코드, 알고리즘, DB 연동과 같은 기능들을 위해 어느 정도 뼈대(구조)를 제공하며 이러한 뼈대 위에서 사용자는 코드를 작성하여 애플리케이션을 개발합니다. 앱/서버 등의 구동, 메모리 관리, 이벤트 루프 등의 공통된 부분은 프레임워크가 관리하며, 사용자는 프레임워크가 정해준 방식대로 클래서, 메서드들을 구현하면 됩니다.  
예시로는 Java 서버 개발에 사용되는 Spring가 있습니다.

라이브러리는 소프트웨어를 개발할 때 컴퓨터 프로그램이 사용하는 특정 기능을 모와둔 코드, 함수들의 집합이며 코드 작성 시 활용 가능한 도구들을 의미합니다.  
예시로는 JQuery가 있습니다.

프레임워크와 라이브러리의 차이점은 "제어 흐름"의 권한이 어디에 있는가입니다.  
라이브러리를 사용할 때 사용자는 애플리케이션 코드의 흐름을 직접 제어해야 합니다.  
개발 시 필요한 기능이 있을 경우 능동적으로 라이브러리를 호출하여 사용하거나 기존에 구성된 함수나 코드를 가져다 써야 합니다.  
반면 프레임워크는 애플리케이션의 코드가 프레임워크에 의해 사용됩니다.  
애플리케이션 코드는 프레임워크가 짜 놓은 틀에서 수동적으로 동작하기 때문에 제어의 흐름은 프레임워크가 가지고 있고 사용자가 그 안에 필요한 코드를 작성하게 됩니다.

<br>

### \[Q\] Spring vs Spring Boot

\[A\]  
가장 큰 차이점은 Auto Configuration의 차이입니다.(환경설정 자동화) Spring은 프로젝트 초기에 다양한 환경설정을 해야 하지만, Spring Boot는 설정의 많은 부분을 자동화하여 사용자가 편하게 스프링을 활용할 수 있도록 돕습니다.  
spring boot starter dependency만 추가해주면 설정은 끝나고, 내장된 톰캣을 제공해 서버를 바로 실행할 수 있습니다.

<br>

### \[Q\] Spring의 특징

\[A\]  
경량 컨테이너로서 자바 객체를 직접 관리한다. 각각의 객체 생성, 소멸과 같은 라이프 사이클을 관리하며 스프링으로부터 필요한 객체를 얻어올 수 있다.  
스프링은 Plain Old Java Object 방식의 프레임워크이다. 일반적인 J2EE 프레임워크에 비해 구현을 위해 특정한 인터페이스를 구현하거나 상속을 받을 필요가 없어 기존에 존재하는 라이브러리 등을 지원하기에 용이하고 객체가 가볍다.  
스프링은 제어 반전(IoC : Inversion of Control)을 지원한다. 컨트롤의 제어권이 사용자가 아니라 프레임워크에 있어서 필요에 따라 스프링에서 사용자의 코드를 호출한다.  
스프링은 의존성 주입(DI : Dependency Injection)을 지원한다. 각각의 계층이나 서비스들 간에 의존성이 존재할 경우 프레임워크가 서로 연결시켜준다.  
스프링은 관점 지향 프로그래밍(AOP : Aspect-Oriented Programming)을 지원한다. 따라서 트랜잭션이나 로깅, 보안과 같이 여러 모듈에서 공통적으로 사용하는 기능의 경우 해당 기능을 분리하여 관리할 수 있다.  
스프링은 영속성과 관련된 다양한 서비스를 지원한다. iBATIS나 하이버네이트 등 이미 완성도가 높은 데이터베이스 처리 라이브러리와 연결할 수 있는 인터페이스를 제공한다.  
스프링은 확장성이 높다. 스프링 프레임워크에 통합하기 위해 간단하게 기존 라이브러리를 감싸는 정도로 스프링에서 사용이 가능하기 때문에 수많은 라이브러리가 이미 스프링에서 지원되고 있고 스프링에서 사용되는 라이브러리를 별도로 분리하기도 용이하다.

<br>

### \[Q\] POJO (Plain Old Java Object) 란?

\[A\]  
체 지향적인 원리에 충실하면서 환경과 기술에 종속되지 않고 필요에 따라 재활용될 수 있는 방식으로 설계된 오브젝트를 말한다. 그러한 POJO에 애플리케이션의 핵심로직과 기능을 담아 설계하고 개발하는 방법을 POJO 프로그래밍이라고 할 수 있다.

<br>

### \[Q\] PSA (Portable Service Abstraction) 란?

\[A\]  
PSA란 환경의 변화와 관계없이 일관된 방식의 기술로의 접근 환경을 제공하는 추상화 구조를 말합니다.  
이는 POJO 원칙을 철저히 따른 Spring의 기능으로 Spring에서 동작할 수 있는Library들은 POJO원칙을 지키게끔 PSA형태의 추상화가 되어있음을 의미합니다.

<br>

### \[Q\] DI (Dependency Insection) 란?

\[A\]  
의존성 주입은 필요한 객체를 직접 생성하는 것이 아닌 외부로부터 객체를 받아서 사용하는 것입니다.  
이를 통해 객체간의 결합도를 줄이고 코드의 재사용성을 높일 수 있습니다.

의존성 주입은 생성자 주입, 필드 주입, 세터 주입의 3 가지 방법이 있습니다.  
이 중 Spring에서 가장 권장하는 의존성 주입 방법은 생성자를 통한 주입 방법입니다.  
그 이유는 순환 참조를 방지하고 불변성을 가지며 테스트에 용이하기 때문입니다.

<br>

### \[Q\] 의존성이란?

\[A\]  
파라미터나 리턴값 또는 지역변수 등으로 다른 객체를 참조하는 것 입니다.

<br>

### \[Q\] 의존성 주입 방법

\[A\]  
생성자 주입(Constructor Injection), 필드 주입(Field Injection), 수정자 주입(Setter Injection)이 있습니다.

그 중 가장 권장하는 방법은 생성자를 통한 주입입니다.  
그 이유는 순환 참조를 방지할 수 있고 불변성을 가지고 있어 런타임에서 의존성을 주입받는 객체가 변할 일이 없어지게 됩니다.

<br>

### \[Q\] IoC (Inversion of Control 제어역전)란?

\[A\]  
제어의 역전(IoC)이란 모든 객체에 대한(생성, 라이프사이클 등) 제어권을 개발자가 아닌 IoC 컨테이너에게 넘긴 것을 말합니다.  
스프링에서는 IoC 컨테이너에 객체(bean)들을 생성하면 객체끼리 의존성을 주입(DI, Dependency Injection)하는 역할을 합니다.

<br>

### \[Q\] Spring Container란?

\[A\]
스프링 컨테이너는 스프링에서 자바 객체들을 관리하는 공간을 말합니다. 자바 객체의 생명 주기를 관리하며, 생성된 자바 객체들에게 추가적인 기능을 제공합니다.

<br>

### \[Q\] Spring Bean란?

\[A\]
스프링에서는 자바 객체를 빈(Bean)이라 한다.

<br>

### \[Q\] Spring Bean life Cycle

\[A\]  
스프링 Bean의 LifeCycle은 스프링 IoC 컨테이너 생성 → 스프링 빈 생성 → 의존관계 주입 → 초기화 콜백 메소드 호출 → 사용 → 소멸 전 콜백 메소드 호출 → 스프링 종료

스프링은 크게 3가지 방법으로 빈 생명주기 콜백을 관리합니다.

1.  인터페이스( InitializingBean, DisposableBean )
2.  설정 정보에 초기화 메소드, 종료 메소드 지정
3.  @PostConstruct, @PreDestroy 어노테이션 지원

<br>

### \[Q\] Spring Bean 등록 방법

\[A\]  
빈을 등록하는 방법은 2가지가 있습니다.

1.  우선 가장 쉬운 방법으로 @Component 어노테이션을 사용하는 것입니다.  
    @Controller, @Service, @Repository는 모두 @Component를 포함하고 있습니다.
2.  설정 클래스를 따로 만들어 @Configuration 어노테이션을 붙이고,  
    해당 클래스 안에서 빈으로 등록할 메소드를 만들어 @Bean 어노테이션을 붙여주면 자동으로 해당 타입의 빈 객체가 생성됩니다.

<br>

### \[Q\] AOP (Aspect Oriented Programming)란?

\[A\]  
AOP는 핵심 비즈니스 로직에 있는 공통 관심사항을 분리하여 각각을 모듈화 하는 것을 의미하며 공통 모듈인 인증, 로깅, 트랜잭션 처리에 용이합니다. AOP의 가장 큰 특징이자 장점은 중복 코드 제거, 재활용성의 극대화, 변화수용의 용이성이 좋다는 점입니다.

핵심 비즈니스 로직에 부가기능을 하는 모듈이 중복되어 분포되어 있을 경우 사용할 수 있습니다.

<br>

### \[Q\] @RequestBody vs @RequestParam vs @ModelAttribute

\[A\]  
@RequestBody는 클라이언트가 전송하는 JSON 형태의 HTTP Body 내용을 MessageConverter를 통해 Java Object로 변환시켜주는 역할을 합니다.  
값을 주입하지 않고 값을 변환 시키므로(Reflection을 사용해 할당), 변수들의 생성자, Getter,Setter가 없어도 정상적으로 할당됩니다.

@RequestParam은 1개의 HTTP 요청 파라미터를 받기 위해 사용합니다. @RequestParam은 필수 여부가 true이기 때문에,기본적으로 반드시 해당 파라미터가 전송되어야 합니다. 전송되지 않으면 400Error가 발생할 수 있으며 ,반드시 필요한 변수가 아니라면 required의 값을 false로 설정해줘야 합니다.

@ModelAttribute는 HTTP Body 내용과 HTTP 파라미터의 값들을 생성자,Getter,Setter를 통해 주입하기 위해 사용합니다. 값 변환이 아닌 값을 주입시키므로 변수들의 생성자나 Getter,Setter가 없으면 변수들이 저장되지 않습니다.

<br>

### \[Q\] Spring MVC 패턴이란?

\[A\]  
MVC는 Model, View, Controller의 약자이며, 각 레이어간 기능을 구분하는데 중점을 둔 디자인 패턴입니다.  
View는 비즈니스 로직의 처리 결과를 유저에게 보여주는 역할을 합니다. (html, jsp, tymeleaf, mustache 등 화면을 구성하기도 하고, Rest API로 서버가 구현된다면 json 응답으로 구성되기도 한다.)  
Model은 데이터 관리 및 비즈니스 로직을 처리하는 부분이며, (DAO, DTO, Service 등)  
Controller는 View에서 받은 사용자의 요청을 Model에 전달해주고 Model이 처리한 결과를 다시 View로 반환해주는 중개 역할을 합니다. Model과 View는 서로 연결되어 있지 않기 때문에 Controller가 사이에서 통신 매체가 되어줍니다.

<br>

### \[Q\] Lombok이란?

\[A\]  
Lombok은 Java 기반에서 기계적으로 작성하는 VO, DTO, Entity 관련 작업을 쉽게 할 수 있게 해주는 라이브러리 입니다.  
Lombok을 이용하면 Getter, Setter, ToString, hashCode 등의 메소드들을 간편하게 사용할 수 있게 해줍니다.  
Spring 프로젝트에서 사용할 경우 JPA 환경과 함께 일관화 되고 가독성이 좋은 어플리케이션을 작성할 수 있습니다.

** Lombok이 만드는 메소드들이 생성되는 시점 **  
Lombok은 메소드를 컴파일 하는 과정에 개입해서 추가적인 코드를 만들어냅니다. 이것을 어노테이션 프로세싱이라고 하는데, 어노테이션 프로세싱은 자바 컴파일러가 컴파일 단계에서 어노테이션을 분석하고 처리하는 기법을 말합니다.  
(Lombok 라이브러리를 추가할 때 CompileOnly, AnnotationProcessor를 추가하는 이유도 된다.)

<br>

### \[Q\] Entity vs DTO vs VO vs BO vs DAO

\[A\]  
Entity는 실제 DataBase의 테이블과 1 : 1로 매핑되는 클래스로, DB의 테이블내에 존재하는 컬럼만을 속성(필드)으로 가져야 합니다.  
DTO(Data Transfer Object)는 각 계층간의 데이터 교환을 위한 객체로 주로 비동기 처리를 할 때 사용합니다. (여기서 말하는 계층은 Controller, View, Business Layer, Persistent Layer)  
VO(Value Object)는 실제 데이터만을 저장하는 객체를 말합니다. 오직 read만 가능하며 getter만 사용 가능하여 주로 데이터가 불변이어야 하고, 단순히 저장된 값을 불러와야 하는 경우 사용합니다.  
BO(Business Object)는 여러 DAO를 활용해 비즈니스 로직을 처리하는 객체를 말합니다. (Service에 해당)  
DAO(Data Access Object)는 DB의 데이터에 접근을 위한 객체를 말합니다. (Repository 또는 Mapper에 해당)

<br>

### \[Q\] JPA (Java Persistence API) 란?

\[A\]
JPA란 자바 진영의 ORM 기술 표준을 의미한다.
즉, ORM(Object Relational Mapping)을 사용해 데이터베이스에서 지속적으로 많은 양의 데이터를 관리하기 위한 API를 의미한다.