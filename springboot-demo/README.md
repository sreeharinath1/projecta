# Spring Boot Employee Manager – Sample Project
<img width="1440" height="558" alt="image" src="https://github.com/user-attachments/assets/779ed379-f76a-4d69-a88e-01677631e663" />



#👨‍💻 About Me
Hello! I am a passionate on Tech. Let's connect through Pipeline #Devops

A complete Spring Boot web application demonstrating:
- Thymeleaf web UI (CRUD pages)
- REST API (`/api/employees`)
- JPA + H2 in-memory database
- Bean Validation
- Unit Tests (Mockito + MockMvc)
- Integration Tests (REST Assured + @DataJpaTest)

---🎨 Version Architecture Guide
This workspace features three distinct versions of the application, iterating on UI/UX design paradigms.

1. 💡 emp-dir-v1 (Light & Clean Theme)
Design Focus: Clean professional light mode with crisp corporate aesthetics, standard table layout, and subtle borders.
Best for: Standard enterprise office setups preferring high-brightness corporate dashboards.
2. 🌌 emp-dir-v2 (Dark Neon Mode)
Design Focus: Deep space dark mode (#0b0f19) with glowing neon cyan, warning orange, and vibrant pink buttons.
Best for: Engineering command centers and developer-focused environments.
3. 🪟 emp-dir-v3 (Ultimate Dynamic Glassmorphism & Theme Switcher)
Design Focus: Premium glassmorphic design featuring animated gradient backgrounds (@keyframes gradientBG), floating elements, 3D hover cards on the landing page (index.html), and a Persistent Floating Theme Switcher

## Project Structure

```
springboot-demo/
├── pom.xml
└── src/
    ├── main/
    │   ├── java/com/example/demo/
    │   │   ├── DemoApplication.java          # Entry point
    │   │   ├── DataSeeder.java               # Seeds sample data
    │   │   ├── controller/
    │   │   │   ├── HomeController.java        # Redirects / → /employees
    │   │   │   ├── EmployeeController.java    # Thymeleaf web controller
    │   │   │   └── EmployeeRestController.java# REST API controller
    │   │   ├── service/
    │   │   │   └── EmployeeService.java       # Business logic
    │   │   ├── repository/
    │   │   │   └── EmployeeRepository.java    # JPA repository
    │   │   ├── model/
    │   │   │   └── Employee.java              # JPA entity
    │   │   └── exception/
    │   │       ├── ResourceNotFoundException.java
    │   │       └── GlobalExceptionHandler.java
    │   └── resources/
    │       ├── application.properties
    │       ├── static/css/style.css
    │       └── templates/employees/
    │           ├── list.html
    │           ├── form.html
    │           ├── detail.html
    │           └── error.html
    └── test/
        ├── java/com/example/demo/
        │   ├── service/
        │   │   └── EmployeeServiceTest.java        # Unit – service layer
        │   ├── controller/
        │   │   ├── EmployeeRestControllerTest.java  # Unit – REST (MockMvc)
        │   │   └── EmployeeControllerTest.java      # Unit – web (MockMvc)
        │   └── integration/
        │       ├── EmployeeApiIT.java               # Integration – full HTTP
        │       └── EmployeeRepositoryIT.java         # Integration – JPA layer
        └── resources/
            └── application-test.properties
```

---

## Requirements

- **Java 17+**
- **Maven 3.8+**

---

## Running the App

```bash
mvn spring-boot:run
```

Open: http://localhost:8080

H2 Console: http://localhost:8080/h2-console
- JDBC URL: `jdbc:h2:mem:demodb`
- Username: `sa` / Password: *(empty)*

---

## Running Tests

```bash
# Unit tests only
mvn test

# Integration tests only
mvn failsafe:integration-test

# All tests (unit + integration)
mvn verify
```

---

## REST API Endpoints

| Method | Endpoint                            | Description              |
|--------|-------------------------------------|--------------------------|
| GET    | /api/employees                      | List all employees       |
| GET    | /api/employees/{id}                 | Get employee by ID       |
| POST   | /api/employees                      | Create new employee      |
| PUT    | /api/employees/{id}                 | Update employee          |
| DELETE | /api/employees/{id}                 | Delete employee          |
| GET    | /api/employees/department/{dept}    | Filter by department     |

---

## Web Pages

| URL                        | Description          |
|----------------------------|----------------------|
| /employees                 | List all employees   |
| /employees/new             | Add employee form    |
| /employees/{id}            | Employee detail view |
| /employees/edit/{id}       | Edit employee form   |
| /employees/delete/{id}     | Delete employee      |

---

## Test Coverage Summary

| Test Class                    | Type        | Tests |
|-------------------------------|-------------|-------|
| EmployeeServiceTest           | Unit        | 9     |
| EmployeeRestControllerTest    | Unit        | 10    |
| EmployeeControllerTest        | Unit        | 7     |
| EmployeeApiIT                 | Integration | 10    |
| EmployeeRepositoryIT          | Integration | 9     |
| **Total**                     |             | **45**|

## Built with ❤️ using Spring Boot & Thymeleaf 
## Just for learning #DevOps #Java
# Not for production usage   ---------------Any One can use this project
                                                                        #SREE
