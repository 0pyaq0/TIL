# 🎈 정적(static) vs. 비정적(non-static)
<br><br>

### <span style = 'color: red'>'다른 클래스'</span> 에서 정의된 메소드
- ###### 비정적 소속변수나 비정적 소속메소드를 호출하기 위해서는 우선 객체가 생성되어 있어야 한다.
- ###### 정적 소속변수에 접근하거나 정적 소속메소드를 호출하는 경우에는 객체를 생성하지 않아도 됨

<br>

#### <span style = 'background-color: #fff5b1'>호출방식</span>
- 비정적 소속변수: 객체이름 . 소속변수이름
  - ``` Car c = new Car(); ```
  - ``` String str = c.color ; ```
  <br>
- 정적 소속변수: 클래스이름 . 소속변수이름
  - ``` int n = Car.numberOfCars ;  ```
  <br>
- 비정적 소속메소드 : 객체이름 . 메소드이름 (…) 
  - ``` Car c = new Car(); ```
  - ``` String str = c.toString(); ```
  <br>
- 정적 소속메소드 : 클래스이름 . 메소드이름 (...) 
  - ``` Car.increase(); ```
  <br><br>

- - -
<br>

### <span style = 'color: red'>'같은 클래스'</span> 에서 정의된 메소드
<br>

- ##### 비정적 메소드
  - 같은 클래스 내부에 정의된 비정적/정적 소속변수 모두 참조 가능
  - 같은 클래스 내부에 정의된 비정적/정적 소속메소드 모두 호출 가능
  - 호출 시에는 메소드 이름만을 사용

<br>

- ##### 정적 메소드
  - 같은 클래스 내부에 정의된 <span style = 'background-color: #fff5b1'>**정적 소속변수만**</span> 참조 가능
  - 같은 클래스 내부에 정의된 <span style = 'background-color: #fff5b1'>**정적 소속메소드만** </span> 호출 가능
  - 호출 시에는 메소드 이름만을 사용