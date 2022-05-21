# <img src = "/Kotlin/img/kotlin_icon.png" width=35> Kotlin
<br><br>

### 코틀린 (Kotlin ) 이란?
> 2011년 7월 JetBrains사가 공개한 JVM에서 동작하는 프로그래밍 언어로서, <span style = 'background-color: #fff5b1'>
**간결하고 실용적이며 자바코드와의 상호운용성을 중시한 언어**</span> 이다.

현재 자바가 사용되고 있는 모든 용도에 적합하면서도 더 간결하고 생산적이며 안전한 대체 언어를 제공하는 것을 목적으로 두고 있다.

<br>

- - -
<br>

### 🎈 주요 특성
<br>

#### <span style = 'background-color: #f1f8ff'>대상 플랫폼

- 서버상의 코드
- 안드로이드 디바이스에서 실행되는 모바일 애플리케이션

<br>

#### <span style = 'background-color: #f1f8ff'>타입 (type)
##### 정적 타입(statically typed) 지정 언어
> **정적 타입 지정**은 모든 프로그래밍 구성 요소의 타입을 컴파일 시점에 알 수 있고 프로그램 안에서 객체의 필드나 메소드를 사용할 때마다 컴파일러가 **타입을 검증** 해준다는 뜻

<br>

##### 정적 타입 지정 언어의 장점
- **🔥 성능**
  - 실행 시점에 어떤 메소드를 호출할지 알아내는 과정이 필요 없으므로 메소드 호출이 더 빠르다.
    ```
    // 정적 타입 ( Java, Kotlin 등)
    a.call()  // 객체 a의 클래스의 call 메소드 ( 컴파일 단계에서 알고 있음 ) 
    
    // 동적 타입 ( JavaScript, python 등 ) 
    b.call()  // 누구의 call 메소드 ? ( 컴파일 단계에서 알 수 없음 ) 
    ```
    <br>
- **🫂 신뢰성**
  - 컴파일러가 프로그램의 정확성을 검증하기 때문에 실행 시 프로그램이 오류로 중단될 가능성이 더 적어진다.
  <br>
- **🪜 유지 보수성**
  - 코드에서 다루는 객체가 어떤 타입에 속하는지 알 수 있기 때문에 처음보는 코드를 다룰 때도 더 쉽다.
  <br>
- **🛠️ 도구 지원**
  - 도구는 더 정확한 코드 완성 기능을 제공할 수 있으며, IDE의 다른 지원 기능도 **동적 타입 지정 언어**에 비해 더 잘 만들 수 있다.

<br>

#### <span style = 'background-color: #f1f8ff'>타입 추론 ( type inference )
대부분 코틀린 컴파일러가 문맥으로부터 변수 타입을 자동으로 유추할 수 있기 때문에 타입 선언을 생략해도 된다.
```
var x = 1  // Int
var y = 7.5e6  // 7.5 X 10^6 = 7500000.0 :: Double
```
<br>

#### <span style = 'background-color: #f1f8ff'>널이 될 수 있는 타입 ( nullable type )
코틀린은 null이 될 수 있는 타입을 지원함에 따라 컴파일 시점에 **null pointer exception**이 발생할 수 있는지 여부를 검사할 수 있다.
```
// **?** : null 가능
var a: String? = null
var b: String? = "bbb"
b = null

// null 불가능
var c: String = "ccc"
c = null  // compile error ( Null can not be a value of a non-null type String )
var d: String = null  // compile error ( Null can not be a value of a non-null type String )
```
<br>

#### <span style = 'background-color: #f1f8ff'>함수형 프로그래밍 ( functional programming )
##### 핵심 개념
- **일급 객체( first-class )인 함수**
  - 함수를 일반 값처럼 다룰 수 있다.
    ```
    // 함수를 변수에 저장
    val test: () -> Unit = { println("kotlin") }

    // 함수를 인자로 다른 함수에 전달
    fun test(func: () -> Unit) {
        func()
    }

    // 함수에서 함수를 반환
    fun test() : () -> Unit {
	    { println("kotlin") }
    }
    ```
    <br>
- **불변성 ( immutability )**
  - 함수형 프로그래밍에서는 일단 만들어지고 나면 내부 상태가 절대로 바뀌지 않는 불변 객체를 사용해 프로그램을 작성한다.
  <br>
- **부수 효과 ( side effect ) X**
  - 함수형 프로그래밍에서는 입력이 같으면 항상 같은 출력을 내놓고 다른 객체의 상태를 변경하지 않으며, 함수 외부나 다른 바깥 환경과 상호작용하지 않는 <br> **순수 함수(pure function)** 를 사용한다.
    ```
    // 순수 함수 
    fun getSum(a: Int, b: Int) = a + b

    // 순수하지 않은 함수
    var a = 1
    fun getSum(c: Int) = a + c
    ```
    <br><br>

##### 이점
- **🖥️ 간결성**
  - 명령형(imperative) 코드에 비해 더 간결하며 우아하다. 순수 함수를 값처럼 활용할 수 있으면 더 강력한 추상화할 수 있고 강력한 추상화를 사용해 코드 중복을 막을 수 있다.
  <br>
- **🚫 Thread safe**
  - 불변 데이터 구조를 사용하고 순수 함수를 데이터 구조에 적용한다면 <br>다중 스레드 환경에서 같은 데이터를 여러 스레드가 변경할 수 없다.
  <br>
- **🧪 테스트 용이**
  - side effect가 있는 함수는 그 함수를 실행하기 위해 필요한 환경을 구성하는 준비 코드(setup code)가 필요하지만 순수 함수는 준비 코드 없이 독립적인 테스트가 가능하다.

  <br><br>

- - -
<br>

### 📖 철학
<br>

#### 실용성

#### 간결성

#### 상호운용성

<br><br>

- - -
<br>

### 🌐 코틀린 코드 컴파일
<br>

```
kotlinc <소스파일 또는 디렉터리> -include-runtime -d <jar 이름>
java -jar <jar 이름>
```

#### Kotlin Runtime Library
- Kotlin 프로젝트 빌드 과정
  <img src = "/Kotlin/img/Kotlin Runtime Library.png">
  코틀린 컴파일러로 컴파일한 코드는 코틀린 런타임 라이브러리에 의존한다. 이 라이브러리에는 코틀린 자체 표준 라이브러리 클래스와 자바 API의 기능을 확장한 내용이 있다. 코틀린 컴파일한 애플리케이션을 배포할 때는 런타임 라이브러리도 함께 배포해야 한다.
  <br>
- Java 코드와 Kotlin 코드가 섞여 있는 프로젝트 컴파일 과정
  <img src = "/Kotlin/img/Java_Kotlin.png">
  - Kotlin 컴파일러가 Kotlin 코드를 컴파일해 .class 파일을 생성한다. 이 과정에서 Kotlin 코드가 참조하는 Java 코드가 함께 로딩되어 사용된다.
  - Java 컴파일러가 Java 코드를 컴파일해 .class 파일을 생성한다. 이때 이미 Kotlin이 컴파일한 .class 파일의 경로를 클래스 패스에 추가해 컴파일한다.

<br>
- - -
<br>



#### 참고
- https://kotlinlang.org/