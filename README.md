# ph-jaxb-pom

A POM only project that contains all dependencies for easily using JAXB from Maven.

Currently it is very tedious to include all artefacts relevant for JAXB into each and every POM manually.
Therefore I created this project to provide an easy to use POM for using JAXB from within Maven.

This project is can be used for JAXB 2.2.x and 2.3.x.
JAXB 2.3.x is only targeting Java 9 and newer. 

# News and noteworthy

* v1.0.1 - 2019-01-15
    * Updated to JAXB 2.3.2 for JDK 9+
* v1.0.0 - 2018-11-21
    * Initial release for JAXB 2.2.11 and 2.3.1

# Maven usage

Include it in your regular Maven dependencies but explicitly state the type **pom**:

```xml
<dependency>
  <groupId>com.helger</groupId>
  <artifactId>ph-jaxb-pom</artifactId>
  <version>1.0.1</version>
  <type>pom</type>
</dependency>
```

---

My personal [Coding Styleguide](https://github.com/phax/meta/blob/master/CodingStyleguide.md) |
On Twitter: <a href="https://twitter.com/philiphelger">@philiphelger</a>
