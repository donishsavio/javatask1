# First Project Java Spring

A simple Spring Boot REST application built with Java and Maven, created as part of university labs at Akademia Finansów i Biznesu Vistula.



## Technologies

| Technology     | Version  |
|----------------|----------|
| Java           | 17+      |
| Spring Boot    | 3.x      |
| Maven          | 3.x      |
| IntelliJ IDEA  | 2024+    |

---

## Project Structure

```
first-project-java-spring/
├── src/
│   └── main/
│       └── java/
│           └── pl/edu/vistula/firstprojectjavaspring/
│               ├── FirstProjectJavaSpringApplication.java
│               └── controller/
│                   └── HelloController.java
├── pom.xml
└── README.md
```

---

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/first-project-java-spring.git
cd first-project-java-spring
```

### 2. Run using Maven
```bash
mvn spring-boot:run
```

### 3. Or run directly in IntelliJ IDEA
- Open the project in IntelliJ IDEA
- Navigate to `FirstProjectJavaSpringApplication.java`
- Click the green ▶ **Run** button

### 4. The application starts on:
```
http://localhost:8080
```
<img width="512" height="512" alt="vistula" src="https://github.com/user-attachments/assets/260bee62-538e-4513-93cd-f2a8c8074e92" />



## Use Cases & HTTP Methods

### ✅ Use Case 1 — Hello Controller

**Endpoint:** `GET /`  
**Description:** Returns a welcome message from the first Spring REST controller.  
**HTTP Method:** `GET`  
**URL:** `http://localhost:8080/`

#### Request
```
GET http://localhost:8080/
```

#### Response
```
Hello Vistula, in my first Spring controller.
```

#### How to test

**Option A — Browser:**
- Open your browser and go to `http://localhost:8080/`
- You will see the response text displayed directly in the browser

> 📸 **Screenshot:** *(add a screenshot of the browser showing the response)*

**Option B — IntelliJ HTTP Client (generated-requests.http):**
```http
GET http://localhost:8080/
```
- Open the `.http` file in IntelliJ
- Click the green ▶ button next to the request
- The response will appear in the **Run** panel

> 📸 **Screenshot:** *(add a screenshot of the IntelliJ HTTP client with the response)*

**Option C — curl (terminal):**
```bash
curl -X GET http://localhost:8080/
```

Expected output:
```
Hello Vistula, in my first Spring controller.
```

> 📸 **Screenshot:** *(add a screenshot of the terminal showing the curl output)*

---

## Controller Code

**File:** `src/main/java/pl/edu/vistula/firstprojectjavaspring/controller/HelloController.java`

```java
package pl.edu.vistula.firstprojectjavaspring.controller;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping(value = "/")
    public String hello() {
        return "Hello Vistula, in my first Spring controller.";
    }
}
```

### Annotation explanations

| Annotation        | Purpose                                                                 |
|-------------------|-------------------------------------------------------------------------|
| `@RestController` | Marks the class as a REST controller; returns data directly (not a view)|
| `@GetMapping("/")`| Maps HTTP GET requests at path `/` to the `hello()` method             |



## Author

Donish savio Doomanik
