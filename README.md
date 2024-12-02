## Test your created SpringBoot Hello World
It defines a simple Spring Boot application with a REST controller that maps the /hello endpoint to a method returning a personalized greeting based on an optional name query parameter.

<br />

## Test your JDK
#### Go to the demo directory
```bash
cd TestJava
```
```bash
cd demo
```

<br/>

#### Check your Java version
```bash
java --version
```
```
openjdk 22.0.1 2024-04-16
OpenJDK Runtime Environment (build 22.0.1+8-16)
OpenJDK 64-Bit Server VM (build 22.0.1+8-16, mixed mode, sharing)
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

<br />

## Test your localhost
Link: ```http://localhost:8080/hello```

<br />

Output:

<img width="346" alt="Screenshot 2024-12-02 at 3 33 16 PM" src="https://github.com/user-attachments/assets/8458a0cf-c53f-4efd-b27b-f4811724822a">
