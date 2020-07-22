# DevOps-Basic
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.thinknyx.demo</groupId>
  <artifactId>liquorshop</artifactId>
  <packaging>war</packaging>
  <version>1.0</version>
  <name>Liquor Shop Demo</name>
  <url>https://thinknyx.com</url>
    
  <properties>
    <sonar.projectKey>kmayer10_liquor-shop-demo</sonar.projectKey>
      <sonar.organization>kmayer10</sonar.organization>
      <sonar.host.url>https://sonarcloud.io</sonar.host.url>
      <sonar.login>faff74d8cb559ee0ed1500446f12b3918db42332</sonar.login>
  </properties>
    
  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>
    <!-- https://mvnrepository.com/artifact/org.eclipse.equinox/javax.servlet -->
    <dependency>
        <groupId>javax.servlet</groupId>
        <artifactId>javax.servlet-api</artifactId>
        <version>3.0.1</version>
        <scope>provided</scope>
    </dependency>
    
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-core</artifactId>
        <version>5.0.1.RELEASE</version>
    </dependency>

  </dependencies>
  
    <distributionManagement>
        <repository>
            <id>github</id>
            <name>GitHub OWNER Apache Maven Packages</name>
            <url>https://maven.pkg.github.com/kmayer10/epsilon</url>
        </repository>
    </distributionManagement>
    <build>
        <finalName>LiquorShop</finalName>
        <plugins>
            <plugin>
                <groupId>org.apache.tomcat.maven</groupId>
                <artifactId>tomcat7-maven-plugin</artifactId>
                <version>2.2</version>
                <configuration>
                    <port>8081</port>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.owasp</groupId>
                <artifactId>dependency-check-maven</artifactId>
                <version>5.3.2</version>
                <executions>
                    <execution>
                        <goals>
                            <goal>check</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>            
        </plugins>
    </build>
</project>
