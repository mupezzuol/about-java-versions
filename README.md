# Java versions and their main news for developers.:heart_eyes:

Project used to know a little about what is best in Java versions.

## Index :pushpin:

- [Java 9](#java9)
- [Java 10](#java10)
- [Java 11](#java11)
- [Java 12](#java12)
- [Java 13](#java13)
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

.....

## Java 12 <a name="java12"></a>:heart:

.....

## Java 12 <a name="java12"></a>:heart:

.....

## References - Versions and Release Date <a name="references"></a> :link:

- References: _[Wikipedia](https://en.wikipedia.org/wiki/Java_version_history). (2020-02-25)_ 
![Java Version](img/java-version.png)
