xxs공격 
===
WebInitialization클래스 작성중 검색하다 찾은 공격 
XXS 크로스 사이트 스크립트, 클라이언트를 대상으로 한 공격으로 게시판이나 JS등 스크립트 코드를 삽입해서 렌더링 과정에서 몰래 기능이 작동하게한다. 
* Stored
* Reflected
네이버 luck xxs방어법 사용하면 된다고 한다. 다음에 써봐야겠다.

public class WebInitialization  extends AbstractAnnotationConfigDispatcherServletInitializer

public class "" extends EnableWebMvc



This looks like one of the differences between our old AnnotationMethodHandlerAdapter implementation and our 3.1+ RequestMethodHandlerAdapter. Indeed, for all practical purposes, you should always use @EnableWebMvc which leads to the use of our modern-day infrastructure. For backwards compatibility with 2.5 and 3.0 based applications, DispatcherServlet still uses the old variant if no explicit configuration is given. Note that this will be streamlined as of 5.0, with the old infrastructure getting removed then.

If you are using XML based configuration then use <mvc:annotation-driven/> as an alternative to @EnableWebMvc

@EnableWebMvc and <mvc:annotation-driven /> have the same purpose, mixing them doesn't work in some cases.

AnnotationMethodHandlerAdapter 구현과 3.1 이상의 RequestMethodHandlerAdapter 간의 차이점 중 하나로 보입니다. 실제로 모든 실제적인 목적을 위해 항상 @EnableWebMvc를 사용해야 하며, 이는 오늘날의 인프라를 사용할 수 있습니다. 2.5 및 3.0 기반 애플리케이션과의 이전 버전과의 호환성을 위해 명시적 구성이 제공되지 않은 경우에도 DispatcherServlet은 이전 버전을 사용합니다. 5.0부터는 기존 인프라가 제거되면서 간소화가 이루어집니다.

XML 기반 구성을 사용하는 경우 @EnableWebMvc의 대안으로 <mvc:annotation-driven/>을 사용합니다.

@EnableWebMvc와 <mvc:notation-driven />의 목적은 동일하며, 혼합하는 것은 경우에 따라 효과가 없습니다.



