# study.java

## Maven

### user-specific settings

https://maven.apache.org/settings.html

```console
$ cp ${maven.home}/conf/settings.xml ~/.m2/
```

### Maven in 5 Minutes

```console
$ mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
$ cd my-app
$ mvn package
...
[ERROR] Source option 1.5 is no longer supported. Use 1.6 or later.
[ERROR] Target option 1.5 is no longer supported. Use 1.6 or later.
...
```

https://github.com/spring-guides/gs-maven/issues/21

```xml:pom.xml
<properties>
  <java.version>1.9</java.version>
  <maven.compiler.source>${java.version}</maven.compiler.source>
  <maven.compiler.target>${java.version}</maven.compiler.target>
</properties>
```

```console
$ mvn package
$ java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App
Hello World!
```
