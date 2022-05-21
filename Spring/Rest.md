# 🌐 Rest
<br>

## Rest (Representational State Transfer)
 - **자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것**
 <br>
 - HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원(URI)에 대한,<br>  **CRUD Operation** 을 적용하는 것을 의미합니다. 
 <br>

   > **CRUD Operation**
     대부분의 컴퓨터 소프트웨어가 가지는 기본적인 데이터 처리 기능 <br>
     **Create** : 데이터 생성(POST)
     **Read** : 데이터 조회(GET)
     **Update** : 데이터 수정(PUT)
     **Delete** : 데이터 삭제(DELETE)

<br>

- - -
<br>

### REST 구성 요소
<br>

1. 자원(Resource) : HTTP URI <br>
2. 자원에 대한 행위(Verb) : HTTP Method <br>
3. 자원에 대한 행위의 내용 (Representations) : HTTP Message Pay Load

<br>

- - -
<br>

### REST의 특징
<br>

1. Server-Client(서버-클라이언트 구조)
2. Stateless(무상태)
3. Cacheable(캐시 처리 가능)
4. Layered System(계층화)
5. Uniform Interface(인터페이스 일관성)

<br>

- - -
<br>

### REST의 장단점

<br>

#### 장점

- HTTP 프로토콜의 인프라를 그대로 사용하므로 REST API 사용을 위한 <br> 별도의 인프라를 구출할 필요가 없다.
<br>

- HTTP 프로토콜의 표준을 최대한 활용하여 여러 추가적인 장점을 함께 가져갈 수 있게 해 준다.
<br>

- HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다.
<br>

- Hypermedia API의 기본을 충실히 지키면서 범용성을 보장한다.
<br>

- REST API 메시지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악할 수 있다.
<br>

- 여러 가지 서비스 디자인에서 생길 수 있는 문제를 최소화한다.
<br>

- 서버와 클라이언트의 역할을 명확하게 분리한다.
<br><br><br>

#### 단점

- 표준이 자체가 존재하지 않아 정의가 필요하다.
<br>

- 사용할 수 있는 메소드가 4가지밖에 없다.
<br>

- HTTP Method 형태가 제한적이다.
<br>

- 브라우저를 통해 테스트할 일이 많은 서비스라면 쉽게 고칠 수 있는 URL보다 Header 정보의 값을 처리해야 하므로 전문성이 요구된다.
<br>

- 구형 브라우저에서 호환이 되지 않아 지원해주지 못하는 동작이 많다. (익스폴로어)





