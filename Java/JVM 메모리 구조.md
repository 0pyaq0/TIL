# 🔎 JVM 메모리 구조
<br><br>

### 1️. method area 
> JVM이 .class파일을 읽어 클래스별로 필드데이터, 메소드 데이터, 메소드 코드, 
생성자 코드 등을 분류해 저장

<br>
<center>
<img src = "/Java/img/method_area.png">
</center>
<br>

- 전역변수, static 붙은 메소드, 클래스 변수(static 붙은 변수) 저장
- 클래스가 로딩될 때 생성되고, 모든 스레드가 공유하는 영역
- 클래스가 실제로 호출될때 method area에 올라감
- 프로그램의 시작부터 종료가 될 때까지 메모리에 남아있게 됨

<br><br><br>

### 2. call stack
> 메소드를 위한 작업공간 

<br>
<center>
<img src = "/Java/img/call_stack.png">
</center>
<br>

- main이 제일 먼저 수행되어 밑에 존재
- 메소드가 실행되는 동안 객체 참조변수, 지역변수와 연산의 중간결과를 저장
- 메소드가 끝나면 메모리 반환

<br><br><br>

### 3. heap
> new 연산자로 생성된 객체와 배열 저장

<br>
<center>
<img src = "/Java/img/heap.png">
</center>
<br>

- 클래스 영역에 선언된 인스턴스 변수들 저장
- 자바에서는 garbage collector가 관리