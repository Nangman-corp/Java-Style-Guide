# Java Style Guide

<aside>
💡 본문은 낭만(Nangman)의 Java 스타일 가이드 입니다. 구글 Java 가이드를 참고하여 작성하였습니다.

</aside>

---
## 목차

### [1. 소개(Intro)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#1-%EC%86%8C%EA%B0%9Cintro-1)
- [1.1 용어(term)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#11-%EC%9A%A9%EC%96%B4term)
### [2. 이름(Name)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#2-%EC%9D%B4%EB%A6%84name-1)
- [2.1 공통 규칙(common rules)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#21-%EA%B3%B5%ED%86%B5-%EA%B7%9C%EC%B9%99common-rules)
- [2.2 파일(File)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#22-%ED%8C%8C%EC%9D%BCfile)
- [2.3 패키지(Package)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#23-%ED%8C%A8%ED%82%A4%EC%A7%80package)
- [2.4 클래스(Class)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#24-%ED%81%B4%EB%9E%98%EC%8A%A4class)
- [2.5 상수(Constant)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#25-%EC%83%81%EC%88%98constant)
- [2.6 메소드(Method)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#26-%EB%A9%94%EC%86%8C%EB%93%9Cmethod)
- [2.7 변수(Variable)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#27-%EB%B3%80%EC%88%98variable)
### [3. 포맷(Format)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#3-%ED%8F%AC%EB%A7%B7format-1)
- [3.1 소스코드 구조(Source code Structure)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#31-%EC%86%8C%EC%8A%A4%EC%BD%94%EB%93%9C-%EA%B5%AC%EC%A1%B0source-code-structure)
- [3.2 중괄호(Braces)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#32-%EC%A4%91%EA%B4%84%ED%98%B8braces)
- [3.3 줄(Line)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#33-%EC%A4%84line)
- [3.4 공백 문자(Blank)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#34-%EA%B3%B5%EB%B0%B1-%EB%AC%B8%EC%9E%90blank)
- [3.5 어노테이션(Annotation)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#35-%EC%96%B4%EB%85%B8%ED%85%8C%EC%9D%B4%EC%85%98annotation)
- [3.6 제어자 순서(Modifier Ordinary)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#36-%EC%A0%9C%EC%96%B4%EC%9E%90-%EC%88%9C%EC%84%9Cmodifier-ordinary)
- [3.7 리터럴(Literal)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#37-%EB%A6%AC%ED%84%B0%EB%9F%B4literal)
### [4. 프로그래밍 관례(Programming Practices)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#4-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-%EA%B4%80%EB%A1%80programming-practices-1)
- [4.1 @Override는 무조건 사용(@Override : always used)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#41-override%EB%8A%94-%EB%AC%B4%EC%A1%B0%EA%B1%B4-%EC%82%AC%EC%9A%A9override--always-used)
- [4.2 모든 예외는 처리(Caught exceptions : not ignored)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#42-%EB%AA%A8%EB%93%A0-%EC%98%88%EC%99%B8%EB%8A%94-%EC%B2%98%EB%A6%ACcaught-exceptions--not-ignored)
- [4.3 Static 멤버는 클래스로 접근(Static members : Qualified using class)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#43-static-%EB%A9%A4%EB%B2%84%EB%8A%94-%ED%81%B4%EB%9E%98%EC%8A%A4%EB%A1%9C-%EC%A0%91%EA%B7%BCstatic-members--qualified-using-class)

---

# 1. 소개(Intro)

---

본 문서는 Nangman의 Java code 스타일을 설명합니다. 본 문서의 가이드를 이해하신 후 사용하시는 기술 문서(Spring, Android)로 이동하여 기술에 해당하는 가이드를 숙지하세요!

## 1.1 용어(term)

---

1. 클래스(Class) 용어는 아래를 의미합니다.
    - 일반적인 클래스
    - 열거형 클래스 - Enum Class
    - 인터페이스 - Interface
    - 어노테이션 타입 - Annotation type( @interface )
2. 클래스 멤버( Class Member ) 용어는 아래를 의미합니다.
    - 중첩된 클래스 - Nested Class
    - 필드 - Field
    - 메서드 - Method
    - 생성자 - Constructor
3. 주석(Comments) 용어는 아래를 의미합니다.
    - 주석 - Comment(s) : 소스코드 내 구현 주석

<aside>
💡 문서형 주석을 설명할 때는 Document Comments 라는 용어는 사용하지 않고, Javadoc이 라는 일반적인 용어를 사용합니다.

</aside>

# 2. 이름(Name)

### 2.1 공통 규칙(**common rules)**

---

- 모든 식별자는 ASCII와 숫자만 허용합니다.
- 식별자에 접미사와 접두사는 허용하지 않습니다.

```
(예시)
(X) name_ 
(X) mName 
(X) s_name 
(X) kName 
```

### 2.2 파일(File)

---

- 최상위 클래스 이름과 동일하게 대소문자를 구별하여 작성(다른 파일과 중복된 이름을 가진 클래스 파일은 허용하지 않습니다.)
- .java파일 만 허용합니다.
- 소스파일은 UTF-8 인코딩을 지원합니다.
- 코드의 가독성이 높다고 판단되면 유니코드 인코딩을 사용할 수 있습니다.

### 2.3 패키지(**Package)**

---

- 소문자와 숫자만 사용가능합니다.

```
(예시)
(O) com.example.deepspace 
(X) com.example.deepSpace 
(X) com.example.deep_space 
```

### 2.4 클래스(Class)

---

- 클래스 이름은 [UpperCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case) 로 작성됩니다.
- 클래스 이름은 일반적으로는 명사, 명사구로 작성합니다.

```
(클래스 예시)
(O) CompanyList
(X) Companylist
```

- 인터페이스의 경우 일부 형용사, 형용사 구를 포함할 수 있습니다.

```
(인터페이스 예시)
(O) CompanyReliableRate
(O) CompanyTrustRate
(X) CompanyLiability
```

- 테스트 클래스의 경우 해당 클래스 이름 뒤에 Test를 포함합니다

```
(예시)
(O) CompanyListTest
```

### 2.5 상수(**Constant**)

---

- 대문자와 언더바가 허용되는 UPPER_SNAKE_CASE를 사용합니다.
- 명사, 명사구로 작성해야합니다.

```
(예시)
(O) MAX_MONEY
```

### 2.6 메소드(Method)

---

- [lowerCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)를 사용하며 동사 또는 동사구 입니다.

```
(예시)
(O) sendMessage
(O) stop
(X) companyList
(O) editCompanyList
```

### 2.7 변수(Variable)

---

매개변수, 지역변수, 유형 변수를 포함합니다.

- [lowerCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)를 사용하며 명사 또는 명사구 입니다.
- 공용 메소드에서 한 문자 매개변수 이름은 피해야 합니다.
- 지역변수는 최종적이고 변경할 수 없는 경우에도 지역 변수는 상수로 간주되지 않으며 상수로 스타일이 지정되어서는 안 됩니다.
- 유형(Generic) 변수는 단일 대문자, 선택적으로 단일 숫자(예: `E`, `T`, `X`, `T2`)로 사용합니다.

```
(예시)
(O) maxAge
(O) Request
```

# 3. 포맷(Format)

### 3.1 소스코드 구조(Source code Structure)

---

1. 라이센스
2. Package 문
3. Import 문
4. 소스코드 개요 등 코멘트
5. Class 선언

<aside>
💡 각 섹션 사이에는 공백 라인이 하나 들어갑니다.

</aside>

### 3.2 중괄호(Braces)

---

Kernighan & Ritchie Style에서 변형된 one true brace style (****OTBS)** 방식을 따릅니다.

```java
return () -> {
  while (condition()) {
    method();
  }
};

return new MyClass() {
  @Override public void method() {
    if (condition()) {
      try {
        something();
      } catch (ProblemException e) {
        recover();
      }
    } else if (otherCondition()) {
      somethingElse();
    } else {
      lastThing();
    }
    int x = foo();
    frob(x);
  }
};
```

- if 절의 경우 단 한줄이어도 중괄호를 반드시 사용해야합니다.
- 단, 코드가 없는 메소드는 바로 닫는 것을 허용합니다.

```java
(예시)
...
void method(){}
...
```

### 3.3 줄(**Line)**

---

- 들여쓰기는 스페이스 4개를 기준으로 합니다.
- 줄 길이는 100개의 문자로 제한합니다.
- 줄 바꿈은 상황에 따라 적절하게 활용합니다.

<aside>
💡 심볼이 있는 경우 심볼 앞에서 줄 바꿈하는 것을 권장합니다.

</aside>

- 여러문장이 내려온 경우 첫번째 내려온 문장과 동일한 들여쓰기를 유지합니다.

```java
(예제)
List<Integer> numbers = Arrays.asList(1, 2, 1, 3, 3, 2);
    numbers.stream()
        .filter(i -> i % 2 == 0)
        .distinct()
        .forEach(System.out::println);

AnnotationConfigApplicationContext ac = 
            new AnnotationConfigApplicationContext(SameBeanConfig.class);
```

### 3.4 공백 문자(**Blank)**

---

- if, for, catch 와 ( 사이에 공백문자 삽입.
- else와 catch ‘}’사이에 공백문자 삽입.
- , 다음에 공백문자 삽입.
- 예약어 내에서 사용하는 ; 뒤에는 공백문자 삽입.
- infix 연산자의 경우 앞, 뒤로 공백문자 삽입.

```java
Boolean test = true;
if (test) {
	//...
} else {
	//...
}
int testNum = 2 + 1 * (4 / 2) - 25;

for (int i = 0; i < 3; i++) {
	//        
}
```

### 3.5 어노테이션(Annotation)

---

- 들여쓰기 적용하지 않음
- 유형-사용 어노테이션(Type-use annotations)
- 사용할 식별자 앞에서 정의하여 사용 가능. 어노테이션이 메타 어노테이션인 경우 유형-사용 어노테이션으로 간주함.
- ex : @Target(ElementType.TYPE_USE)

```java
final @Nullable String name;

public @Nullable Person getPersonByName(String name);

@NotNull
public Person person
```

- 클래스 어노테이션(Class annotations)
- 클래스 선언 윗 줄 혹은 라인앞에 사용가능

```java
@Override
@Nullable
public String getNameIfPresent() { ... }

@Partial @Mock DataLoader loader;
```

### 3.6 제어자 순서(Modifier Ordinary)

---

- 각 제어자가 동시에 사용되는 경우 아래 순서에 따름

```java
public protected private abstract default static final transient volatile synchronized native strictfp
```

### 3.7 리터럴(Literal)

---

- 대문자 사용

```
(예시)
(O) 30000000L
(X) 30000000l
```

# 4. 프로그래밍 관례(****Programming Practices)****

### 4.1 @Override는 무조건 사용(@Override : always used)

---

- 오버라이딩이 된 모든 경우에는 필수 기입함
- 부모 쪽에서 @Deprecated를 선언한 경우 자식 쪽 생략 가능

### 4.2 모든 예외는 처리(Caught exceptions : not ignored)

---

- 모든 예외는 필수로 처리한다
- 만약 예외를 처리하지 않는 경우에는 그 이유에 대해 명확히 주석을 첨부함
- 테스트 코드에서는 필요 시 무시 가능

### 4.3 Static 멤버는 클래스로 접근(Static members : Qualified using class)

---

- 클래스 명으로 접근한다.

```java
Foo aFoo = ...;
Foo.aStaticMethod(); // good
aFoo.aStaticMethod(); // bad
somethingThatYieldsAFoo().aStaticMethod(); // very bad
```

<aside>
💡 본문은 [구글 Java 스타일 가이드](https://google.github.io/styleguide/javaguide.html#s6-programming-practices)를 참고하였으며, 이후 사용하는 기술 문서를 추가로 확인해주세요 🙂

</aside>

---

[Spring Style Guide](https://www.notion.so/Spring-Style-Guide-176f99976b7e4d42a31aca4c70873748)
