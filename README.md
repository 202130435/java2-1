# 허동민 202130435

## 3월 22일 강의 
새 프로젝트  
ctrl + shift + p >> java create new project >> no build tools >> 자기 이름으로 된 파일 디렉토리 설정 >> java21로 파일 설정후 새로운 프로젝트 설정  

새로운 프로젝트를 쓰고 싶으면 깃허브에 저장된 디렉토리를 새로 설정해서 README.md파일에 푸쉬만 해놓으면 된다.  

java21폴더 안에 있는 vscode,bin,lib,src폴더 4개를 복사해서 기존 java2-1폴더로 붙여넣기한후 커밋해서 푸쉬하기.  

프로그래밍 언어  
(1)프로그램 작성 언어  
기계어(machine language),어셉블리어(assembly language)  

프로그래밍과 컴파일  
소스: 프로그래밍 언어로 작성된 텍스트 파일  
컴파일:소스 파일을 컴퓨터가 이해할 수있 는 기계어로 만드는 과정  

자바의 태동  
1991년 그린 프로젝트-선마이크로시스템즈의 제임스 고글링에 의해 시작  

목적  
플랫폼 호환성 문제 해결, 플랫폼 독립적인 언어 개발, 메모리 사용량이 적고 다양한 플랫폼을 가지는 가전제품에 적용  

WORA(Write Once Run Anywhere)  
한번 작성된 코드는 모든 플랫폼에서 바로 실행되는 자바의 특징  
1) 바이트 코드  
2) JVM(Java Virtual Machine)  

JDK  
개발자용 프로그램  
JRE  
개발자가 아니고 단순하게 프로그램 실행만 할때 사용하는 프로그램  

``` java
public class Test {
    public static void main(String[] args) {
        System.out.println("Hello");
    }
}
```

자바소스 컴파일  
파일 탐색기에서 좌측 상단에 파일 클릭후 윈도우 파워쉘 들어가서 자바 파일의 코드를 보고 싶으면 javac Test.java, 자바 파일을 컴파일 하고 싶으면 java test.java를 입력해서 확인하면 된다.    

서블릿  
웹 서버에서 실행되는 자바 프로그램  
서블릿을 이번 수업떄 배울건 아니므로 패스  

자바 모바일 응용: 안드로이드 앱  
안드로이드  
-구글의 주도로 여러 모바일 회사가 모여 구성한 OHA(Open Handset Alliance)에서 개발한
무료 모바일 플랫폼  

자바의 특징

-플랫폼 독립성  
자바는 독립적인 바이트 코드로 컴파일되며 JVM만 있으면 자바 프로그램의 실행가능  
-객체 지향  
캡슐화, 상속, 다형성 등을 지원하며 해결할 과제를 실제 세상의 객체와 객체간의 상호
관계로 모델링하여 인간의 사고에 가깝게 표현한다.  
-클래스로 캡슐화  
변수나 메소드를 클래스내에 구현하며 클래스안에 내부 클래스 구현도 가능하다.  
-소스와 클래스 파일  
컴파일된 클래스 안에는 반드시 하나의 자바 클래스만 들어있다. 하나의 자바코드에 클래스를 여러개 컴파일할 경우 할 때마다 별도의 클래스가 생성된다.  
-실행 코드 배포  
자바 응용프로그램은 한 개의 클래스 파일 또는 다수의 클래스 파일로 구성된다.  
-패키지  
서로 관련있는 클래스는 패키지로 묶어 관리한다. 파일 시스템의 폴더 개념과 같다.  
-멀티스레드  
하나의 자바 프로그램에서 다수의 스레드가 동시에 실행할 수 있는 환경 지원  
-가비지 컬렉션  
램내에 사용되지 않는 메모리는 가비지 컬렉션에 의해서 자동으로 회수된다.  
-실시간 응용프로그램에 부적합  
가비지 컬렉션 자동 실행 > 프로그램 실행 일시 중단 > 실시간 부적합하다  
-자바 프로그램은 안전  
타입체크가 엄격하며, 포인터의 개념이 없기 때문에 시스템이 중단되는 일은 없다.  
-프로그램 작성 쉬움  
-실행 속도 개선을 위한 JIT 컴파일러 사용  


자바 프로그램의 구조  
Chapter21.java 
``` java
// 예제2-1
public class Chapter21 {
    public static void main(String[] args) {
        public static int sum(int n,int m) {
           s = sum(n , m)
        }
    }
}

```
주석 키= ctrl+/

```java
public class App {
    public static void main(String[] args) throws Exception {
        System.out.println("println1");
        System.out.println("println2");
        System.out.println("print1");
        System.out.println("print2");
    }
}
```
식별자 (idetifier)  
클래스, 변수, 상수, 메소드에 붙이는 이름을 말한다.

자바의 데이터 타입
기본 타입 :8개
boolean  
char  
byte  
short  
int  
long  
float  
double  
레퍼런스 타입:1개
-배열에 관한 레퍼런스  
-클래스에 대한 레퍼런스  
-인터페이스에 대한 레퍼런스  

문자열 
문자열은 기본 타입이 아님  
String 클래스로 문자열 표현
``` java
public class App {
    public static void main(String[] args) throws Exception {
        System.out.println("print " + 13 + 1.14 + "???");
    }
}

```

변수  
-프로그램 실행 중에 값을 임시 저장하기 위한 공간  
변수 선언  
-데이터 타입에서 정한 크기의 메모리 할당  

리터럴(Literal)  
-프로그램에서 직접 표현한 값  
-정수, 실수, 문자, 논리, 문자열 리터럴 있음  

정수 리터럴  
-10진수, 8진수, 16진수, 2진수 리터럴  
-정수 리터럴은 int형으로 리터럴  

실수 리터럴  
-소수점 형태나 지수 형태로 표현한 실수  
-실수 타입 리터럴은 더블 타입으로 리터럴  

문자 리터럴  
-단일 인용부로('')로 문자 표현  
-특수문자 리터럴은 백슬래시(\)로 시작  

논리 타입 리터럴  
-논리 값 표시  
-true, false 두개밖에 없고 boolean 타입의 변수에 직접 치환하거나 조건문에 사용한다  

var 키워드  
java 10부터 도입  
기존의 변수 선언 방식 : 변수의 타입 반드시 지정  
var 키워드  
-타입을 생략하고 변수 선언 가능  
-컴파일러가 추론하여 변수 타입 결정  
-변수 선언 시 초깃값이 주어지지 않으면 컴파일 오류  
-var은 지역 변수 선언에만 한정  

```java
public class App {
    public static void main(String[] args) throws Exception {
       var foo = 200;
       var name = "woogle";
       
       System.out.println("foo + name")
    }
}
```


## 3월 15일 강의
내용 정리

깃 로그인 하고   
터미널에 유저 네임하고 이메일 입력해놓고 확인하기  
저장 하고 제목 @월 @@일로 입력하고 커밋하기  
커밋한거 깃으로 푸쉬하기   
깃 배쉬 익스텐션 깔기  
이쁘게 잘 꾸미기??  

항상 텍스트 치고 스페이스바 두번 누르는것 잊지 말기.  
OpenJDK (ms버전 21)설치  
이클립스 실행해서 Hello 파일 생성한 후에 Hello.java 파일 만들기  
자바는 vscode로만 진행  
자바 익스텐션 설치하고 Hello.java 파일 만들기  
+Test.java 파일 만들기  
만든 파일 커밋후 푸쉬하기  
자바 파일 업로드 할때는 ``` ``` 사이에 코드 집어넣고 ```옆에 자바면 java 파이썬이면 Python 입력하기  

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello");
    }
}
```