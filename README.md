# ph-jaxb-pom

A POM only project that contains all dependencies for easily using JAXB from Maven.

Currently it is very tedious to include all artefacts relevant for JAXB into each and every POM manually.
Therefore I created this project to provide an easy to use POM for using JAXB from within Maven.

This project is can be used for JAXB 2.2.x and 2.3.x.
JAXB 2.3.x is only targeting Java 9 and newer. 

# News and noteworthy

* v2.0.0 - work in progress
    * Updated to JAXB 4.0.0
    * Requires Java 11 as the baseline
* v1.2.2 - 2021-10-31
    * Updated to JAXB 2.3.5
* v1.2.0 - 2021-05-02
    * Removed `<dependencies>` to enforce using it as a BOM
* v1.1.0 - 2020-09-17
    * Switching to Jakarta version 2.3.3 - no more differentiation
* v1.0.3 - 2019-05-07
    * Using unbounded version instead of limiting to Java 12.x
* v1.0.2 - 2019-05-02
    * Added support for JDK 12
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
  <version>1.2.0</version>
  <type>pom</type>
  <scope>import</scope>
</dependency>
```

# Gradle usage (for issues up to v1.0.3)

As Gradle does not support Maven profile activation by JDK version, this section outlines the includes per JDK version (as of ph-jaxb-pom 1.0.1).

With JDK 8, include the following dependencies:
* org.glassfish.jaxb:jaxb-core:2.2.11
* org.glassfish.jaxb:jaxb-runtime:2.2.11
* com.sun.istack:istack-commons-runtime:2.21

With JDK 9 or later, include the following dependencies:
* org.glassfish.jaxb:jaxb-runtime:2.3.2

The exclusion of this POM might be necessary via `exclude group: 'com.helger', module: 'ph-jaxb-pom'`

---

My personal [Coding Styleguide](https://github.com/phax/meta/blob/master/CodingStyleguide.md) |
On Twitter: <a href="https://twitter.com/philiphelger">@philiphelger</a> |
Kindly supported by [YourKit Java Profiler](https://www.yourkit.com)