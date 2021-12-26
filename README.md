# microlam-assembly-descriptor
Shared Assembly Descriptor for AWS Lambda

Add this plugin to your pom.xml

```pom.xml
<plugin>
  <artifactId>maven-assembly-plugin</artifactId>
  <dependencies>
    <dependency>
      <groupId>io.microlam</groupId>
      <artifactId>microlam-assembly-descriptor</artifactId>
      <version>1.2</version>
    </dependency>
  </dependencies>

    <configuration>
      <descriptorRefs>
              <descriptorRef>aws-lambda</descriptorRef>
      </descriptorRefs>
    </configuration>
    
    <executions>
        <execution>
            <id>aws_lambda_deployment_package</id>
            <phase>package</phase>
            <goals>
                <goal>single</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```
