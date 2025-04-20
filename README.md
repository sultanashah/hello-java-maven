# Task 8: Run a Simple Java Maven Build Job in Jenkins

## 🌟 Objective
Set up and run a basic Java Maven build job using Jenkins to understand Continuous Integration (CI) concepts.

## 🧰 Tools Used
- AWS EC2 Instance (Ubuntu)
- Jenkins (Installed via apt)
- Java 11
- Apache Maven
- Git
- Freestyle Jenkins Job

## 📁 Project Structure
```
hello-java-maven/
├── pom.xml
└── src/
    └── main/
        └── java/
            └── HelloWorld.java
```

## 🧱 Application Code

### HelloWorld.java
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}
```

### pom.xml
```xml
<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>hello</artifactId>
  <version>1.0</version>
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</project>
```
## ⚙️ Jenkins Job Configuration
- **Type:** Freestyle Project  
- **Custom Workspace:** `/home/ubuntu/hello-java-maven`  
- **Build Step:** Invoke top-level Maven targets  
  - **Goals:** `clean package`

## ✅ Output
Jenkins Console Output shows:
```
[INFO] BUILD SUCCESS
```
![Screenshot 2025-04-20 053122](https://github.com/user-attachments/assets/52a6ecd8-286c-4d98-8986-dd3e5c036cbd)
.
![Screenshot 2025-04-20 053343](https://github.com/user-attachments/assets/8994b3ce-3ae8-4147-8e9f-d1e10e22711a)
## 📚 What I Learned
- Setting up Java Maven project structure
- Installing and configuring Jenkins
- Creating a Freestyle job in Jenkins
- Running Maven builds via Jenkins
- Troubleshooting permission issues and workspace settings
