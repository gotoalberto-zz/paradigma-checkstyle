====================================
Paradigma Checkstyle 
====================================

This is a work-in-progress prototype for help developers to follow the Best
Coding Practices and measure the code quality.

`checkstyle.xml` contains a checkstyle modules configuration.

Some style checks must be implemented as new modules.
These custom modules dependencies are on [paradigma-checkstyle-modules] (https://github.com/gotoalberto/paradigma-checkstyle-modules) project.

------------------------------------
Checkstyle version: 2.6
------------------------------------

------------------------------------
Configure it on your project
------------------------------------

1. Include a `pluginRepository`section on your `pom.xml` maven project:
```
<pluginRepositories>
    <pluginRepository>
        <id>checkstyle</id>
        <url>http://mvnrepository.com/artifact/</url>
    </pluginRepository>
</pluginRepositories>
```

2. Include `checkstyle.xml` and `paradigma.header` on your classpath.

3. Include checkstyle plugin configuration inner `<build>` pom section: 
```
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-checkstyle-plugin</artifactId>
            <version>2.6</version>
            <configuration>
                <configLocation>src/main/resources/checkstyle/checkstyle.xml</configLocation>
            </configuration>
        </plugin>
    </plugins>
</build>
```

4. Run `mvn checkstyle:checkstyle`
