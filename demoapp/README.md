# Spring Boot Demo Web Application

A simple Spring Boot web application that exposes a REST API with a single endpoint `/hello`, returning the message:

> **"Hello, Spring Boot!"**

---

## 🧰 Prerequisites

Before you begin, ensure you have the following installed:

- **Java JDK:** Version 17 or later  
- **Maven:** Version 3.6 or later  
- **IDE:** IntelliJ IDEA (Community or Ultimate) or any IDE with Spring Boot support  
- **Browser/Postman:** For testing the API

---

## 📁 Project Structure

```

demo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/demo/
│   │   │       ├── DemoApplication.java
│   │   │       └── controller/
│   │   │           └── HelloController.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── pom.xml
├── README.md

````

---

## 🚀 Getting Started

### 1. Clone or Download the Project

```bash
git clone <repository-url>
cd demo
````

If you're not using Git, ensure all files (e.g., `pom.xml`, `src/`) are placed in the same directory.

---

### 2. Open in IntelliJ IDEA

* Launch IntelliJ IDEA.
* Go to `File > Open`.
* Select the folder containing `pom.xml`.
* Open as a **Maven project**.

IntelliJ will auto-resolve all dependencies.

---

### 3. Configure Java SDK

* Go to `File > Project Structure > Project`.
* Set:

  * **Project SDK**: Java 17
  * **Language Level**: 17

---

### 4. Configure Maven (Optional)

* Go to `File > Settings > Build, Execution, Deployment > Build Tools > Maven`
  *(macOS: IntelliJ IDEA > Preferences > Build Tools > Maven)*
* Use the **bundled Maven** or specify a custom installation.

---

## ▶️ Running the Application

### ✅ Method 1: IntelliJ (Recommended)

* Open `src/main/java/com/example/demo/DemoApplication.java`
* Right-click > `Run 'DemoApplication.main()'`

Application will start at:
**[http://localhost:8080](http://localhost:8080)**

---

### ✅ Method 2: Maven

* Open the **Maven** tab (right panel in IntelliJ)
* Expand the project > `Lifecycle`
* Double-click `spring-boot:run`

---

## 🔍 Verify the Endpoint

* Open your browser or Postman
* Navigate to:

```
http://localhost:8080/hello
```

You should see:

```
Hello, Spring Boot!
```

---

## 🐞 Debugging

1. Set a **breakpoint** in `HelloController.java` inside `sayHello()` method.
2. Right-click `DemoApplication.java` > `Debug 'DemoApplication.main()'`
3. Access `http://localhost:8080/hello` to hit the breakpoint.

---

## ⛔ Stopping the Application

* In IntelliJ's **Run/Debug** window, click the red **Stop** button (🟥 square icon).

---

## 🛠️ Troubleshooting

| Issue                   | Solution                                                      |
| ----------------------- | ------------------------------------------------------------- |
| Port 8080 in use        | Set `server.port=8081` in `application.properties`            |
| Maven dependencies fail | Click **Refresh** in the Maven tab or run `mvn clean install` |
| Wrong JDK version       | Set correct JDK (17) in `File > Project Structure > SDKs`     |
| No logs in IntelliJ     | Ensure the **Run console** tab is selected                    |

---

## 📦 Key Dependencies

Defined in `pom.xml`:

* `spring-boot-starter-web` — REST API support
* `spring-boot-starter-test` — Testing support (scope: test)

**Spring Boot Version**: `3.3.4`
**Java Version**: `17`

---


