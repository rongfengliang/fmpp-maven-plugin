# fmpp maven plugin

> fork from dremio build plugin and as one maven plugin package



## Usage

* pom.xml

```xml
<repositories>
    <repository>
      <id>github</id>
      <url>https://maven.pkg.github.com/rongfengliang/fmpp-maven-plugin</url>
      <snapshots>
        <enabled>true</enabled>
      </snapshots>
    </repository>
</repositories>
```

* plugins

```maven
<plugin>
    <groupId>com.rongfengliang</groupId>
    <artifactId>fmpp-maven-plugin</artifactId>
    <version>1.0</version>
    <executions>
        <execution>
            <id>generate-fmpp-sources</id>
            <phase>generate-sources</phase>
            <goals>
                <goal>generate</goal>
            </goals>
            <configuration>
                <config>${project.build.directory}/codegen/config.fmpp</config>
                <output>${project.build.directory}/generated-sources/fmpp</output>
                <templates>${project.build.directory}/codegen/templates</templates>
            </configuration>
        </execution>
    </executions>
</plugin>
```
