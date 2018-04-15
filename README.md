# Config maven plugin for compile Dockerfile Example
**Step for implement**
<br/>
- Config Maven Plugin in pox.xml
_compile source file in`src/main/docker` to base directory_
```
<plugin>
    <artifactId>maven-resources-plugin</artifactId>
    <version>3.0.2</version>
    <executions>
        <execution>
            <id>copy-resources</id>
            <phase>validate</phase>
            <goals>
                <goal>copy-resources</goal>
            </goals>
            <configuration>
                <outputDirectory>${basedir}</outputDirectory>
                <resources>
                    <resource>
                        <directory>${basedir}/src/main/docker/</directory>
                        <includes>
                            <include>Dockerfile</include>
                        </includes>
                        <filtering>true</filtering>
                    </resource>
                </resources>
            </configuration>
        </execution>
    </executions>
</plugin>
```
'oc get all --selector app=appname'