# Run the Project

Each project you'll be working on
does have its own requirements for
running it. Just reading it is
enough for a good beginn inside the
dev process.

## Spring boot projects

These type of projects are simply
ran with Intellij or VSCode by
clicking on the green *run* button,
like any normal Java project.

## Docker

Docker images are ran using docker,
so refer to the [docker's run](https://docs.docker.com/engine/reference/run/)
documentation.

## Maven

Maven is a repo manager but can also
handle scripts. So there's a plethora
of way we can run a Java Project
using it:

- Using custom written/translated
  script ([like here](https://stackoverflow.com/questions/1089285/maven-run-project))

```bash
mvn exec:java -Dexec.mainClass="com.ssegning.ntravl.ntravlserver.App" [-Dexec.args="argument1"] ...
```

- Using core functionality of maven
  like show [here](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

```xml
<project>
    <build>
        <plugins>
            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>exec-maven-plugin</artifactId>
                <version>1.2.1</version>
                <configuration>
                    <mainClass>com.ssegning.ntravl.ntravlserver.App</mainClass>
                    <arguments>
                        <argument>argument1</argument>
                    </arguments>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>
```

## Simple Java

Keep in mind, that we're building a
Jar at the end of the day. So we
expect a simple java command to
work also:

```bash
java -cp target/ntravl-server-1.0-SNAPSHOT.jar com.ssegning.ntravl.ntravlserver.App
```