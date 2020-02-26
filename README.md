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

- Agora possui campo de busca, caso você gere o javadoc do seu projeto, ou pegue um javadoc de terceiro, é possível realizar buscas, facilitando os desenvolvedores ainda mais.

#### JShell

- Com _`JShell`_ temos possibilidade de executar comandos Java via terminal de maneira simples, não precisamos de tantos códigos para começarmos a executar comandos básicos em java.

#### Jigsaw - Java Modularizado

- Agora podemos escrever código de maneira modular, de forma que nós podemos escolher qual pacote do java usaremos em nosso código, por padrão o Java vem com diversos pacotes, desde Strings, IO, etc... porém com Java modular, nós podemos escolher o que queremos usar, dessa forma nosso pacote final seja bem menor e só com o que precisamos. _[(Jigsaw Project)](https://openjdk.java.net/projects/jigsaw/)_

## Java 10 <a name="java10"></a>:heart:

- Releases baseados em tempo._[(JEP 322)](http://openjdk.java.net/jeps/322)_
- Inferência de tipos para variáveis _`locais`_._[(JEP 286)](http://openjdk.java.net/jeps/286)_

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

#### Anotações de tipo em expressões lambda

Antes:
```
(valor, conversorMoeda) -> conversorMoeda.converter(valor);
```

Depois:
```
(@Nonnull var valor, @Nonnull var conversorMoeda) -> conversorMoeda.converter(valor);
```

#### O cliente HTTP do Java ganha uma padronização

- No Java 11, a API está consolidada, foi realizado até mesmo a troca do pacote _`jdk.incubator.http`_ por _`java.net.http`_, implementando um modelo não blocante de comunicação, semelhante ao utilizado pelo Nodejs. Além disso, a API também oferece suporte ao HTTP 1.1/2, o que a torna uma opção muito mais robusta em comparação a API URLConnection.

## Java 12 <a name="java12"></a>:heart:

#### Métodos String (indent and transform)

Indent: colocará uma identação no código com o tamanho de espaço definido por um número.
```java
String msg = "Hello\nWorld!".indent(3);
```

Transform: Podemos chaviar essas chamadas e retornar uma String transformada em novos valores, podemos usar como um 'concat' também.
```java
String msg = "Hello".transform(s -> s + ", World!").transform(String::toUpperCase);
```

#### Switch Expressions. (preview)_[(JEP 325)](http://openjdk.java.net/jeps/325)_

- Não precisamos mais utilizar a palavra _`break`_, podemos separar os valores por vírgula, 

Antes:
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

Depois:
```java
switch (day) {
    case MONDAY, FRIDAY, SUNDAY -> System.out.println("A");
    case TUESDAY                -> System.out.println("B");
    case THURSDAY, SATURDAY     -> System.out.println("C");
    case WEDNESDAY              -> System.out.println("D");
}
```

Switch agora pode retornar valor também:
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

- Switch Expressions functionality continues in preview.[(JEP 325)](http://openjdk.java.net/jeps/325)_
- Text Blocks (Preview).[(JEP 355)](http://openjdk.java.net/jeps/355)_

## Java 14 <a name="java14"></a>:heart:

- In progress...

## References - Versions and Release Date <a name="references"></a> :link:

- References: _[Wikipedia](https://en.wikipedia.org/wiki/Java_version_history). (2020-02-25)_ 
![Java Version](img/java-version.png)
