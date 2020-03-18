# Java versions and their main news for developers.:heart_eyes:

Project used to know a little about what is best in Java versions.

## Index :pushpin:

- [Java 9](#java9)
- [Java 10](#java10)
- [Java 11](#java11)
- [Java 12](#java12)
- [Java 13](#java13)
- [Java 14](#java14)
- [References](#references)

## Java 9 <a name="java9"></a>:heart:

#### JavaDoc

- Now it has a search field, if you generate your project's javadoc, or get a third-party javadoc, you can perform searches, making developers even easier.

#### JShell

- With _`JShell`_ we have the possibility to execute Java commands via terminal in a simple way, we don't need so much code to start executing basic commands in java.

#### Jigsaw - Modularized Java

- Now we can write code in a modular way, so that we can choose which java package we will use in our code, by default Java comes with several packages, from Strings, IO, etc ... however with modular Java, we can choose the that we want to use, that way our final package is much smaller and only with what we need. _[(Jigsaw Project)](https://openjdk.java.net/projects/jigsaw/)_

## Java 10 <a name="java10"></a>:heart:

- Time-based releases._[(JEP 322)](http://openjdk.java.net/jeps/322)_
- Type inference for variables _`locais`_._[(JEP 286)](http://openjdk.java.net/jeps/286)_

```java
public void example() {
    //Java 9
    Integer i = 9;
    String s = "Java ";
    System.out.println(s + i);

    //Java 10
    var x = 10;
    var y = "Java ";
    System.out.println(y + x);
}
```

## Java 11 <a name="java11"></a>:heart:

#### Type annotations in lambda expressions

Before:
```
(valor, conversorMoeda) -> conversorMoeda.converter(valor);
```

After:
```
(@Nonnull var valor, @Nonnull var conversorMoeda) -> conversorMoeda.converter(valor);
```

#### The Java HTTP client gains a standardization

- In Java 11, the API is consolidated, even the exchange of the _`jdk.incubator.http`_ package by _`java.net.http`_ was carried out, implementing a non-blocking communication model, similar to that used by Nodejs . In addition, the API also supports HTTP 1.1 / 2, which makes it a much more robust option compared to the URLConnection API.

## Java 12 <a name="java12"></a>:heart:

#### String Methods (indent and transform)

Indent: will place an indentation in the code with the space size defined by a number.
```java
String msg = "Hello\nWorld!".indent(3);
```

Transform: We can call these calls and return a String transformed into new values, we can use it as a 'concat' as well.
```java
String msg = "Hello".transform(s -> s + ", World!").transform(String::toUpperCase);
```

#### Switch Expressions. (preview)_[(JEP 325)](http://openjdk.java.net/jeps/325)_

- We no longer need to use the word _`break`_, we can separate the values with a comma.

Before:
```java
switch (day) {
    case MONDAY:
    case FRIDAY:
    case SUNDAY:
        System.out.println("A");
        break;
    case TUESDAY:
        System.out.println("B");
        break;
    case THURSDAY:
    case SATURDAY:
        System.out.println("C");
        break;
    case WEDNESDAY:
        System.out.println("D");
        break;
}
```

After:
```java
switch (day) {
    case MONDAY, FRIDAY, SUNDAY -> System.out.println("A");
    case TUESDAY                -> System.out.println("B");
    case THURSDAY, SATURDAY     -> System.out.println("C");
    case WEDNESDAY              -> System.out.println("D");
}
```

Switch can now return value too:
```java
private static String switchNew(Days day){
    return switch (day) {
        case MONDAY, FRIDAY, SUNDAY, TUESDAY  -> "A";
        case THURSDAY, SATURDAY               -> "C";
        default                               -> "D";
    };
}
```

## Java 13 <a name="java13"></a>:heart:

- Switch Expressions functionality continues in preview._[(JEP 325)](http://openjdk.java.net/jeps/325)_
- Text Blocks (Preview)._[(JEP 355)](http://openjdk.java.net/jeps/355)_

## Java 14 <a name="java14"></a>:heart:

- Switch Expressions Release._[(JEP 361)](http://openjdk.java.net/jeps/361)_
- Text Blocks Release. _[(JEP 368)](http://openjdk.java.net/jeps/368)_
- Helpful NullPointerExceptions._[(JEP 358)](http://openjdk.java.net/jeps/358)_
- Pattern Matching for instanceof (Preview)._[(JEP 305)](http://openjdk.java.net/jeps/305)_

Before:
```java
if (obj instanceof String) {
    String s = (String) obj;
    // use s
}
```

After:
```java
if (obj instanceof String s) {
    // now will you use 's' here
}
```

#### Records

- Records (Preview)._[(JEP 359)](http://openjdk.java.net/jeps/359)_

The record is equivalent to a class with:

- A private and final attribute for each informed argument;
- A public constructor that uses all arguments;
- Getters;
- toString;
- equals and hashCode.

To enable this preview, use the following flag:
```
javac --enable-preview --release 14 BankTransaction.java
```

Before:
```java
public class ExempleRecord {
    private final int x;
    private final int y;
    public Ponto(int x, int y) {
        this.x = x;
        this.y = y;
    }
    public int getX() {
        return x;
    }
    public void setX(int x) {
        this.x = x;
    }
    public int getY() {
        return y;
    }
    public void setY(int y) {
        this.y = y;
    }
    @Override
    public String toString() {
        return "Ponto{" +
                "x=" + x +
                ", y=" + y +
                '}';
    }
    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Ponto ponto = (Ponto) o;
        return x == ponto.x &&
                y == ponto.y;
    }
    @Override
    public int hashCode() {
        return Objects.hash(x, y);
    }
}
```

After:
```java
record ExempleRecord(int x, int y) { }
```

## References - Versions and Release Date <a name="references"></a> :link:

- References: _[Wikipedia](https://en.wikipedia.org/wiki/Java_version_history). (2020-02-25)_ 
![Java Version](img/java-version.png)
