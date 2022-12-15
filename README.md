# fmpp maven plugin

> fork from dremio build plugin



## Usage


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