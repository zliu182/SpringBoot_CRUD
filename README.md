## Test your created SpringBoot Hello World
It defines a simple Spring Boot application with a REST controller that maps the /hello endpoint to a method returning a personalized greeting based on an optional name query parameter.

<br />

## Test your localhost
Link: ```http://localhost:8080/hello```

<br />

Output:

<img width="346" alt="Screenshot 2024-12-02 at 3 33 16 PM" src="https://github.com/user-attachments/assets/8458a0cf-c53f-4efd-b27b-f4811724822a">

## Key terms
#### Package
```package com.example.demo;```: Defines the package where this class resides, helping to organize code and avoid name conflicts.

<br />

#### Import library
| **Code**                                            | **Explanation**                                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `import org.springframework.boot.SpringApplication;`| Imports the `SpringApplication` class, which provides a convenient way to bootstrap and launch a Spring application.                                                        |
| `import org.springframework.boot.autoconfigure.SpringBootApplication;` | Imports the `@SpringBootApplication` annotation, which is a combination of: <br> - `@Configuration` (for Java-based configuration), <br> - `@EnableAutoConfiguration` (to enable Spring Boot's auto-configuration), <br> - `@ComponentScan` (to scan for Spring components). |
| `import org.springframework.web.bind.annotation.GetMapping;`| Imports the `@GetMapping` annotation, which maps HTTP GET requests to specific handler methods.                                                                              |
| `import org.springframework.web.bind.annotation.RequestParam;`| Imports the `@RequestParam` annotation, used to bind HTTP request parameters to method parameters.                                                                           |
| `import org.springframework.web.bind.annotation.RestController;`| Imports the `@RestController` annotation, which indicates that the class is a RESTful web service controller.                                                                |

<br />

#### Spring framework
| **Code**                                             | **Type**                   | **Explanation**                                                                                                                          |
|------------------------------------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `@SpringBootApplication`                             | Annotation                 | Marks the class as the entry point for the Spring Boot application and enables auto-configuration.                                       |
| `@RestController`                                    | Annotation                 | Indicates that the class will handle RESTful web requests and automatically serialize responses into JSON or other formats.              |
| `public class DemoApplication {`                     | Class Declaration          | Defines the `DemoApplication` class, which serves as the main application class.                                                         |
| `public static void main(String[] args) {`           | Method Declaration         | Entry point for the Java application. The `main` method starts the Spring Boot application.                                              |
| `SpringApplication.run(DemoApplication.class, args);`| Method Call                | Launches the Spring Boot application by creating a Spring application context and starting the embedded web server.                      |

<br />

#### Controller Layer in the Spring Framework

| **Code**                                                                                              | **Explanation**                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `@GetMapping("/hello")`                                                                                | Maps the `/hello` endpoint to the `hello` method. When a GET request is made to `/hello`, this method is invoked.             |
| `public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {`            | Defines the `hello` method, which takes a `name` parameter from the query string. If `name` is not provided, it defaults to "World". |
| `return String.format("Hello %s!", name);`                                                            | Returns a formatted string, greeting the user by name (or "World" if no name is provided).                                    |

<br />

## DemoApplication.java file
```java
package com.example.demo;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class DemoApplication {
    public static void main(String[] args) {
      SpringApplication.run(DemoApplication.class, args);
    }
    @GetMapping("/hello")
    public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {
      return String.format("Hello %s!", name);
    }
}
```

<br />

## Press the debug button to run
```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.4.0)

2024-12-02T15:30:28.418-05:00  INFO 91633 --- [demo] [           main] com.example.demo.DemoApplication         : Starting DemoApplication using Java 17.0.13 with PID 91633 (/Users/vivianliu/Desktop/Terms/Autumn_2024/WSA_500/Week_9/demo/target/classes started by vivianliu in /Users/vivianliu/Desktop/Terms/Autumn_2024/WSA_500/Week_9/demo)
2024-12-02T15:30:28.420-05:00  INFO 91633 --- [demo] [           main] com.example.demo.DemoApplication         : No active profile set, falling back to 1 default profile: "default"
2024-12-02T15:30:28.783-05:00  INFO 91633 --- [demo] [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port 8080 (http)
2024-12-02T15:30:28.789-05:00  INFO 91633 --- [demo] [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2024-12-02T15:30:28.789-05:00  INFO 91633 --- [demo] [           main] o.apache.catalina.core.StandardEngine    : Starting Servlet engine: [Apache Tomcat/10.1.33]
2024-12-02T15:30:28.813-05:00  INFO 91633 --- [demo] [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2024-12-02T15:30:28.814-05:00  INFO 91633 --- [demo] [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 369 ms
2024-12-02T15:30:28.966-05:00  INFO 91633 --- [demo] [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port 8080 (http) with context path '/'
2024-12-02T15:30:28.972-05:00  INFO 91633 --- [demo] [           main] com.example.demo.DemoApplication         : Started DemoApplication in 0.734 seconds (process running for 1.016)
```
