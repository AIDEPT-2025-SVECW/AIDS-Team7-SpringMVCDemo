Spring Boot Demo Web Application
Overview
This is a simple Spring Boot web application that exposes a REST API with a single endpoint (/hello) returning the message "Hello, Spring Boot!". The project is built using Java 17, Spring Boot, and Maven, and is designed to run in IntelliJ IDEA or any compatible IDE.
Prerequisites

Java JDK: Version 17 or later
Maven: Version 3.6 or later
IDE: IntelliJ IDEA (Community or Ultimate Edition) or any IDE with Spring Boot support
Web Browser or Postman: For testing the API

Project Structure
demo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/demo/
│   │   │       ├── DemoApplication.java
│   │   │       └── controller/
│   │   │           └── HelloController.java
│   │   └── resources/
│   │       ├── application.properties
│   └── test/
├── pom.xml
├── README.md

Setup Instructions

Clone or Download the Project

If using a version control system, clone the repository. Otherwise, ensure all project files (pom.xml, src/, etc.) are in a local directory.


Open in IntelliJ IDEA

Launch IntelliJ IDEA.
Select File > Open and navigate to the project folder (containing pom.xml).
Open the project as a Maven project. IntelliJ will automatically resolve dependencies.


Verify JDK Configuration

Go to File > Project Structure > Project.
Ensure Project SDK is set to Java 17.
Set Project language level to 17.


Check Maven Configuration

Go to File > Settings > Build, Execution, Deployment > Build Tools > Maven (Windows/Linux) or IntelliJ IDEA > Preferences > Build, Execution, Deployment > Build Tools > Maven (macOS).
Ensure Maven is set up (use bundled Maven or a custom installation).



Running the Application

Run via IntelliJ

Open src/main/java/com/example/demo/DemoApplication.java.
Right-click and select Run 'DemoApplication.main()'.
The application will start on http://localhost:8080 (as configured in application.properties).


Run via Maven

Open the Maven tab (right sidebar in IntelliJ).
Expand the project (demo) and navigate to Lifecycle.
Double-click spring-boot:run to start the application.


Verify the Application

Once the application starts, open a browser or Postman.
Navigate to http://localhost:8080/hello.
You should see the response: Hello, Spring Boot!.



Debugging

To debug:
Set a breakpoint in HelloController.java (e.g., in the sayHello method).
Right-click DemoApplication.java and select Debug 'DemoApplication.main()'.
Access http://localhost:8080/hello to hit the breakpoint.



Stopping the Application

In IntelliJ, go to the Run or Debug window.
Click the red Stop button (square icon) to stop the application.

Troubleshooting

Port Conflict: If port 8080 is in use, update server.port in src/main/resources/application.properties (e.g., server.port=8081) and restart.
Dependencies Not Resolved: Click the Refresh button in the Maven tab or run mvn clean install in the terminal.
JDK Issues: Verify the correct JDK (17) is configured in File > Project Structure > SDKs.
Logs Not Visible: Ensure the Run console is selected in IntelliJ.

Dependencies
The project uses the following key dependencies (defined in pom.xml):

spring-boot-starter-web: For building the REST API.
spring-boot-starter-test: For testing (scope: test).
Spring Boot version: 3.3.4
Java version: 17


