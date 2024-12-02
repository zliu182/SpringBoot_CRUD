## Spring Quickstart Guide
Link: https://spring.io/quickstart

<br />

## Start a new Spring Boot project -- start.spring.io 
Link: https://start.spring.io/

<br />

Select the dependencies:
- Spring Web
<br />
<img width="1289" alt="Screenshot 2024-12-02 at 3 15 59 PM" src="https://github.com/user-attachments/assets/1dcafdd3-b9bf-42b6-9bda-9cd2ce97c695">

<br /><br />

## Generate it and download
Upzipped the downloaded file:

<img width="354" alt="Screenshot 2024-12-02 at 3 18 04 PM" src="https://github.com/user-attachments/assets/8d0163af-2585-4f65-9f22-88c8b31f0d4d">

<br /><br />

## Open the new window of VS code

Open the demo directory just downloaded:

<img width="467" alt="Screenshot 2024-12-02 at 3 20 26 PM" src="https://github.com/user-attachments/assets/18ea9c6a-e2d5-4c6b-b4d7-d3ceb0a3945d">

<br /><br />

## Back to VS code

DemoApplication.java file path: ```demo/src/main/java/com/example/demo/DemoApplication.java``` 

<br />

Update the DemoApplication.java file:
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

<br /><br />

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

<br />

## Test your localhost
Link: ```http://localhost:8080/hello```

<br />

Output:

<img width="346" alt="Screenshot 2024-12-02 at 3 33 16 PM" src="https://github.com/user-attachments/assets/8458a0cf-c53f-4efd-b27b-f4811724822a">
















