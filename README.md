# Java Style Guide

<aside>
๐ก ๋ณธ๋ฌธ์ ๋ญ๋ง(Nangman)์ Java ์คํ์ผ ๊ฐ์ด๋ ์๋๋ค. ๊ตฌ๊ธ Java ๊ฐ์ด๋๋ฅผ ์ฐธ๊ณ ํ์ฌ ์์ฑํ์์ต๋๋ค.

</aside>

## ๋ชฉ์ฐจ
---

### [1. ์๊ฐ(Intro)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#1-%EC%86%8C%EA%B0%9Cintro-1)
- [1.1 ์ฉ์ด(term)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#11-%EC%9A%A9%EC%96%B4term)
### [2. ์ด๋ฆ(Name)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#2-%EC%9D%B4%EB%A6%84name-1)
- [2.1 ๊ณตํต ๊ท์น(common rules)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#21-%EA%B3%B5%ED%86%B5-%EA%B7%9C%EC%B9%99common-rules)
- [2.2 ํ์ผ(File)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#22-%ED%8C%8C%EC%9D%BCfile)
- [2.3 ํจํค์ง(Package)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#23-%ED%8C%A8%ED%82%A4%EC%A7%80package)
- [2.4 ํด๋์ค(Class)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#24-%ED%81%B4%EB%9E%98%EC%8A%A4class)
- [2.5 ์์(Constant)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#25-%EC%83%81%EC%88%98constant)
- [2.6 ๋ฉ์๋(Method)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#26-%EB%A9%94%EC%86%8C%EB%93%9Cmethod)
- [2.7 ๋ณ์(Variable)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#27-%EB%B3%80%EC%88%98variable)
### [3. ํฌ๋งท(Format)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#3-%ED%8F%AC%EB%A7%B7format-1)
- [3.1 ์์ค์ฝ๋ ๊ตฌ์กฐ(Source code Structure)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#31-%EC%86%8C%EC%8A%A4%EC%BD%94%EB%93%9C-%EA%B5%AC%EC%A1%B0source-code-structure)
- [3.2 ์ค๊ดํธ(Braces)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#32-%EC%A4%91%EA%B4%84%ED%98%B8braces)
- [3.3 ์ค(Line)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#33-%EC%A4%84line)
- [3.4 ๊ณต๋ฐฑ ๋ฌธ์(Blank)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#34-%EA%B3%B5%EB%B0%B1-%EB%AC%B8%EC%9E%90blank)
- [3.5 ์ด๋ธํ์ด์(Annotation)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#35-%EC%96%B4%EB%85%B8%ED%85%8C%EC%9D%B4%EC%85%98annotation)
- [3.6 ์ ์ด์ ์์(Modifier Ordinary)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#36-%EC%A0%9C%EC%96%B4%EC%9E%90-%EC%88%9C%EC%84%9Cmodifier-ordinary)
- [3.7 ๋ฆฌํฐ๋ด(Literal)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#37-%EB%A6%AC%ED%84%B0%EB%9F%B4literal)
### [4. ํ๋ก๊ทธ๋๋ฐ ๊ด๋ก(Programming Practices)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#4-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-%EA%B4%80%EB%A1%80programming-practices-1)
- [4.1 @Override๋ ๋ฌด์กฐ๊ฑด ์ฌ์ฉ(@Override : always used)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#41-override%EB%8A%94-%EB%AC%B4%EC%A1%B0%EA%B1%B4-%EC%82%AC%EC%9A%A9override--always-used)
- [4.2 ๋ชจ๋  ์์ธ๋ ์ฒ๋ฆฌ(Caught exceptions : not ignored)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#42-%EB%AA%A8%EB%93%A0-%EC%98%88%EC%99%B8%EB%8A%94-%EC%B2%98%EB%A6%ACcaught-exceptions--not-ignored)
- [4.3 Static ๋ฉค๋ฒ๋ ํด๋์ค๋ก ์ ๊ทผ(Static members : Qualified using class)](https://github.com/Nangman-corp/Java-Style-Guide/blob/main/README.md#43-static-%EB%A9%A4%EB%B2%84%EB%8A%94-%ED%81%B4%EB%9E%98%EC%8A%A4%EB%A1%9C-%EC%A0%91%EA%B7%BCstatic-members--qualified-using-class)

---

# 1. ์๊ฐ(Intro)

---

๋ณธ ๋ฌธ์๋ Nangman์ Java code ์คํ์ผ์ ์ค๋ชํฉ๋๋ค. ๋ณธ ๋ฌธ์์ ๊ฐ์ด๋๋ฅผ ์ดํดํ์  ํ ์ฌ์ฉํ์๋ ๊ธฐ์  ๋ฌธ์(Spring, Android)๋ก ์ด๋ํ์ฌ ๊ธฐ์ ์ ํด๋นํ๋ ๊ฐ์ด๋๋ฅผ ์์งํ์ธ์!

## 1.1 ์ฉ์ด(term)

---

1. ํด๋์ค(Class) ์ฉ์ด๋ ์๋๋ฅผ ์๋ฏธํฉ๋๋ค.
    - ์ผ๋ฐ์ ์ธ ํด๋์ค
    - ์ด๊ฑฐํ ํด๋์ค - Enum Class
    - ์ธํฐํ์ด์ค - Interface
    - ์ด๋ธํ์ด์ ํ์ - Annotation type( @interface )
2. ํด๋์ค ๋ฉค๋ฒ( Class Member ) ์ฉ์ด๋ ์๋๋ฅผ ์๋ฏธํฉ๋๋ค.
    - ์ค์ฒฉ๋ ํด๋์ค - Nested Class
    - ํ๋ - Field
    - ๋ฉ์๋ - Method
    - ์์ฑ์ - Constructor
3. ์ฃผ์(Comments) ์ฉ์ด๋ ์๋๋ฅผ ์๋ฏธํฉ๋๋ค.
    - ์ฃผ์ - Comment(s) : ์์ค์ฝ๋ ๋ด ๊ตฌํ ์ฃผ์

<aside>
๐ก ๋ฌธ์ํ ์ฃผ์์ ์ค๋ชํ  ๋๋ Document Comments ๋ผ๋ ์ฉ์ด๋ ์ฌ์ฉํ์ง ์๊ณ , Javadoc์ด ๋ผ๋ ์ผ๋ฐ์ ์ธ ์ฉ์ด๋ฅผ ์ฌ์ฉํฉ๋๋ค.

</aside>

# 2. ์ด๋ฆ(Name)

### 2.1 ๊ณตํต ๊ท์น(**common rules)**

---

- ๋ชจ๋  ์๋ณ์๋ ASCII์ ์ซ์๋ง ํ์ฉํฉ๋๋ค.
- ์๋ณ์์ ์ ๋ฏธ์ฌ์ ์ ๋์ฌ๋ ํ์ฉํ์ง ์์ต๋๋ค.

```
(์์)
(X) name_ 
(X) mName 
(X) s_name 
(X) kName 
```

### 2.2 ํ์ผ(File)

---

- ์ต์์ ํด๋์ค ์ด๋ฆ๊ณผ ๋์ผํ๊ฒ ๋์๋ฌธ์๋ฅผ ๊ตฌ๋ณํ์ฌ ์์ฑ(๋ค๋ฅธ ํ์ผ๊ณผ ์ค๋ณต๋ ์ด๋ฆ์ ๊ฐ์ง ํด๋์ค ํ์ผ์ ํ์ฉํ์ง ์์ต๋๋ค.)
- .javaํ์ผ ๋ง ํ์ฉํฉ๋๋ค.
- ์์คํ์ผ์ UTF-8 ์ธ์ฝ๋ฉ์ ์ง์ํฉ๋๋ค.
- ์ฝ๋์ ๊ฐ๋์ฑ์ด ๋๋ค๊ณ  ํ๋จ๋๋ฉด ์ ๋์ฝ๋ ์ธ์ฝ๋ฉ์ ์ฌ์ฉํ  ์ ์์ต๋๋ค.

### 2.3 ํจํค์ง(**Package)**

---

- ์๋ฌธ์์ ์ซ์๋ง ์ฌ์ฉ๊ฐ๋ฅํฉ๋๋ค.

```
(์์)
(O) com.example.deepspace 
(X) com.example.deepSpace 
(X) com.example.deep_space 
```

### 2.4 ํด๋์ค(Class)

---

- ํด๋์ค ์ด๋ฆ์ [UpperCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case) ๋ก ์์ฑ๋ฉ๋๋ค.
- ํด๋์ค ์ด๋ฆ์ ์ผ๋ฐ์ ์ผ๋ก๋ ๋ช์ฌ, ๋ช์ฌ๊ตฌ๋ก ์์ฑํฉ๋๋ค.

```
(ํด๋์ค ์์)
(O) CompanyList
(X) Companylist
```

- ์ธํฐํ์ด์ค์ ๊ฒฝ์ฐ ์ผ๋ถ ํ์ฉ์ฌ, ํ์ฉ์ฌ ๊ตฌ๋ฅผ ํฌํจํ  ์ ์์ต๋๋ค.

```
(์ธํฐํ์ด์ค ์์)
(O) CompanyReliableRate
(O) CompanyTrustRate
(X) CompanyLiability
```

- ํ์คํธ ํด๋์ค์ ๊ฒฝ์ฐ ํด๋น ํด๋์ค ์ด๋ฆ ๋ค์ Test๋ฅผ ํฌํจํฉ๋๋ค

```
(์์)
(O) CompanyListTest
```

### 2.5 ์์(**Constant**)

---

- ๋๋ฌธ์์ ์ธ๋๋ฐ๊ฐ ํ์ฉ๋๋ UPPER_SNAKE_CASE๋ฅผ ์ฌ์ฉํฉ๋๋ค.
- ๋ช์ฌ, ๋ช์ฌ๊ตฌ๋ก ์์ฑํด์ผํฉ๋๋ค.

```
(์์)
(O) MAX_MONEY
```

### 2.6 ๋ฉ์๋(Method)

---

- [lowerCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)๋ฅผ ์ฌ์ฉํ๋ฉฐ ๋์ฌ ๋๋ ๋์ฌ๊ตฌ ์๋๋ค.

```
(์์)
(O) sendMessage
(O) stop
(X) companyList
(O) editCompanyList
```

### 2.7 ๋ณ์(Variable)

---

๋งค๊ฐ๋ณ์, ์ง์ญ๋ณ์, ์ ํ ๋ณ์๋ฅผ ํฌํจํฉ๋๋ค.

- [lowerCamelCase](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)๋ฅผ ์ฌ์ฉํ๋ฉฐ ๋ช์ฌ ๋๋ ๋ช์ฌ๊ตฌ ์๋๋ค.
- ๊ณต์ฉ ๋ฉ์๋์์ ํ ๋ฌธ์ ๋งค๊ฐ๋ณ์ ์ด๋ฆ์ ํผํด์ผ ํฉ๋๋ค.
- ์ง์ญ๋ณ์๋ ์ต์ข์ ์ด๊ณ  ๋ณ๊ฒฝํ  ์ ์๋ ๊ฒฝ์ฐ์๋ ์ง์ญ ๋ณ์๋ ์์๋ก ๊ฐ์ฃผ๋์ง ์์ผ๋ฉฐ ์์๋ก ์คํ์ผ์ด ์ง์ ๋์ด์๋ ์ ๋ฉ๋๋ค.
- ์ ํ(Generic) ๋ณ์๋ ๋จ์ผ ๋๋ฌธ์, ์ ํ์ ์ผ๋ก ๋จ์ผ ์ซ์(์:ย `E`,ย `T`,ย `X`,ย `T2`)๋ก ์ฌ์ฉํฉ๋๋ค.

```
(์์)
(O) maxAge
(O) Request
```

# 3. ํฌ๋งท(Format)

### 3.1 ์์ค์ฝ๋ ๊ตฌ์กฐ(Source code Structure)

---

1. ๋ผ์ด์ผ์ค
2. Package ๋ฌธ
3. Import ๋ฌธ
4. ์์ค์ฝ๋ ๊ฐ์ ๋ฑ ์ฝ๋ฉํธ
5. Class ์ ์ธ

<aside>
๐ก ๊ฐ ์น์ ์ฌ์ด์๋ ๊ณต๋ฐฑ ๋ผ์ธ์ด ํ๋ ๋ค์ด๊ฐ๋๋ค.

</aside>

### 3.2 ์ค๊ดํธ(Braces)

---

Kernighan & Ritchie Style์์ ๋ณํ๋ one true brace style (****OTBS)** ๋ฐฉ์์ ๋ฐ๋ฆ๋๋ค.

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

- if ์ ์ ๊ฒฝ์ฐ ๋จ ํ์ค์ด์ด๋ ์ค๊ดํธ๋ฅผ ๋ฐ๋์ ์ฌ์ฉํด์ผํฉ๋๋ค.
- ๋จ, ์ฝ๋๊ฐ ์๋ ๋ฉ์๋๋ ๋ฐ๋ก ๋ซ๋ ๊ฒ์ ํ์ฉํฉ๋๋ค.

```java
(์์)
...
void method(){}
...
```

### 3.3 ์ค(**Line)**

---

- ๋ค์ฌ์ฐ๊ธฐ๋ ์คํ์ด์ค 4๊ฐ๋ฅผ ๊ธฐ์ค์ผ๋ก ํฉ๋๋ค.
- ์ค ๊ธธ์ด๋ 100๊ฐ์ ๋ฌธ์๋ก ์ ํํฉ๋๋ค.
- ์ค ๋ฐ๊ฟ์ ์ํฉ์ ๋ฐ๋ผ ์ ์ ํ๊ฒ ํ์ฉํฉ๋๋ค.

<aside>
๐ก ์ฌ๋ณผ์ด ์๋ ๊ฒฝ์ฐ ์ฌ๋ณผ ์์์ ์ค ๋ฐ๊ฟํ๋ ๊ฒ์ ๊ถ์ฅํฉ๋๋ค.

</aside>

- ์ฌ๋ฌ๋ฌธ์ฅ์ด ๋ด๋ ค์จ ๊ฒฝ์ฐ ์ฒซ๋ฒ์งธ ๋ด๋ ค์จ ๋ฌธ์ฅ๊ณผ ๋์ผํ ๋ค์ฌ์ฐ๊ธฐ๋ฅผ ์ ์งํฉ๋๋ค.

```java
(์์ )
List<Integer> numbers = Arrays.asList(1, 2, 1, 3, 3, 2);
    numbers.stream()
        .filter(i -> i % 2 == 0)
        .distinct()
        .forEach(System.out::println);

AnnotationConfigApplicationContext ac = 
            new AnnotationConfigApplicationContext(SameBeanConfig.class);
```

### 3.4 ๊ณต๋ฐฑ ๋ฌธ์(**Blank)**

---

- if, for, catch ์ ( ์ฌ์ด์ ๊ณต๋ฐฑ๋ฌธ์ ์ฝ์.
- else์ catch โ}โ์ฌ์ด์ ๊ณต๋ฐฑ๋ฌธ์ ์ฝ์.
- , ๋ค์์ ๊ณต๋ฐฑ๋ฌธ์ ์ฝ์.
- ์์ฝ์ด ๋ด์์ ์ฌ์ฉํ๋ ; ๋ค์๋ ๊ณต๋ฐฑ๋ฌธ์ ์ฝ์.
- infix ์ฐ์ฐ์์ ๊ฒฝ์ฐ ์, ๋ค๋ก ๊ณต๋ฐฑ๋ฌธ์ ์ฝ์.

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

### 3.5 ์ด๋ธํ์ด์(Annotation)

---

- ๋ค์ฌ์ฐ๊ธฐ ์ ์ฉํ์ง ์์
- ์ ํ-์ฌ์ฉ ์ด๋ธํ์ด์(Type-use annotations)
- ์ฌ์ฉํ  ์๋ณ์ ์์์ ์ ์ํ์ฌ ์ฌ์ฉ ๊ฐ๋ฅ. ์ด๋ธํ์ด์์ด ๋ฉํ ์ด๋ธํ์ด์์ธ ๊ฒฝ์ฐ ์ ํ-์ฌ์ฉ ์ด๋ธํ์ด์์ผ๋ก ๊ฐ์ฃผํจ.
- ex : @Target(ElementType.TYPE_USE)

```java
final @Nullable String name;

public @Nullable Person getPersonByName(String name);

@NotNull
public Person person
```

- ํด๋์ค ์ด๋ธํ์ด์(Class annotations)
- ํด๋์ค ์ ์ธ ์ ์ค ํน์ ๋ผ์ธ์์ ์ฌ์ฉ๊ฐ๋ฅ

```java
@Override
@Nullable
public String getNameIfPresent() { ... }

@Partial @Mock DataLoader loader;
```

### 3.6 ์ ์ด์ ์์(Modifier Ordinary)

---

- ๊ฐ ์ ์ด์๊ฐ ๋์์ ์ฌ์ฉ๋๋ ๊ฒฝ์ฐ ์๋ ์์์ ๋ฐ๋ฆ

```java
public protected private abstract default static final transient volatile synchronized native strictfp
```

### 3.7 ๋ฆฌํฐ๋ด(Literal)

---

- ๋๋ฌธ์ ์ฌ์ฉ

```
(์์)
(O) 30000000L
(X) 30000000l
```

# 4. ํ๋ก๊ทธ๋๋ฐ ๊ด๋ก(****Programming Practices)****

### 4.1 @Override๋ ๋ฌด์กฐ๊ฑด ์ฌ์ฉ(@Override : always used)

---

- ์ค๋ฒ๋ผ์ด๋ฉ์ด ๋ ๋ชจ๋  ๊ฒฝ์ฐ์๋ ํ์ ๊ธฐ์ํจ
- ๋ถ๋ชจ ์ชฝ์์ @Deprecated๋ฅผ ์ ์ธํ ๊ฒฝ์ฐ ์์ ์ชฝ ์๋ต ๊ฐ๋ฅ

### 4.2 ๋ชจ๋  ์์ธ๋ ์ฒ๋ฆฌ(Caught exceptions : not ignored)

---

- ๋ชจ๋  ์์ธ๋ ํ์๋ก ์ฒ๋ฆฌํ๋ค
- ๋ง์ฝ ์์ธ๋ฅผ ์ฒ๋ฆฌํ์ง ์๋ ๊ฒฝ์ฐ์๋ ๊ทธ ์ด์ ์ ๋ํด ๋ชํํ ์ฃผ์์ ์ฒจ๋ถํจ
- ํ์คํธ ์ฝ๋์์๋ ํ์ ์ ๋ฌด์ ๊ฐ๋ฅ

### 4.3 Static ๋ฉค๋ฒ๋ ํด๋์ค๋ก ์ ๊ทผ(Static members : Qualified using class)

---

- ํด๋์ค ๋ช์ผ๋ก ์ ๊ทผํ๋ค.

```java
Foo aFoo = ...;
Foo.aStaticMethod(); // good
aFoo.aStaticMethod(); // bad
somethingThatYieldsAFoo().aStaticMethod(); // very bad
```

<aside>
๐ก ๋ณธ๋ฌธ์ [๊ตฌ๊ธ Java ์คํ์ผ ๊ฐ์ด๋](https://google.github.io/styleguide/javaguide.html#s6-programming-practices)๋ฅผ ์ฐธ๊ณ ํ์์ผ๋ฉฐ, ์ดํ ์ฌ์ฉํ๋ ๊ธฐ์  ๋ฌธ์๋ฅผ ์ถ๊ฐ๋ก ํ์ธํด์ฃผ์ธ์ ๐

</aside>

---

### Contributors
---
[๊ฐ๋ฏผ์ค](https://github.com/Minjun-KANG)์ด ์์ฑํ๊ณ  [๋ฐํ์ฑ](https://github.com/HunSeongPark)์ด ๊ฒ์ํ์์ต๋๋ค. ๋์์ ์ฃผ์  [๋ฐํ์ฑ](https://github.com/HunSeongPark)์๊ฒ ๊ฐ์ฌ ์ธ์ฌ๋ฅผ ๋๋ฆฝ๋๋ค.
- [Contributors](https://github.com/Nangman-corp/Java-Style-Guide/graphs/contributors)
