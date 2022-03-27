# CS122B Homework 1 - The Setup Service

These instructions depend on **IntelliJ IDEA Ultimate**. You can apply for a student license to get this.

#### [Config](#config)
#### [Setup](#setup)
#### [Running a Spring Application](#running-a-spring-application)
#### [Running Spring Tests](#running-spring-tests)

## Config
##### `application.yml`

```yml
spring:
  application:
    name: SetupService

server:
  address: 0.0.0.0
  port: 10010
  error: # These settings are for debugging
    include-exception: true
    include-message: always 

logging:
  file:
    name: ./SetupService.log
```

## Setup
1. In **IntelliJ** go to `File > Open...` and select the template folder.
2. To ensure your Maven dependencies are loaded, go to `View > Tool Windows > Maven`. 
3. A Maven window should appear on the right side of the window.
4. Press the 🔄 button on the top left of the Maven window, a tooltip should read `Reload All Maven Projects`.

## Running a Spring Application
1. Go to the Main class (This is the one at the root of the project module) for example:
```java
@SpringBootApplication
public class BasicService
{
    public static void main(String[] args)
    {
        SpringApplication.run(BasicService.class, args);
    }
}
```
2. IntelliJ should add a green arrow to the left of `public class BasicService` press this and click `Run 'BasicService'`


## Running Spring Tests
1. Go to the Main Test class (This is the one at the root of the project test module) for example:
```java
@SpringBootTest
@AutoConfigureMockMvc
public class BasicServiceTest
```
2. IntelliJ should add a green arrow to the left of `public class BasicServiceTest` press this and click `Run 'BasicServiceTest'`
3. You can also test individual tests by pressing the green arrow by any `@Test` method. 
    - Make sure if the tests require a database to set up the `Edit configuration templates...` to ensure that the environment variables are added by default
