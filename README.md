# Student Management System

A Java Spring Boot REST API for managing student records using CRUD operations. This project demonstrates REST API development, database integration, validation, pagination, and exception handling.

## Features

- Create, retrieve, update, and delete student records
- Retrieve student details by ID
- Search students by city and course
- Paginated student retrieval
- Input validation
- Global exception handling
- MySQL database integration

## Technologies Used

- Java 17+
- Spring Boot 3.x
- Spring Web
- Spring Data JPA
- MySQL
- Maven
- Jakarta Validation
- Git and GitHub
- Postman for API testing

## Project Structure

```text
src/
├── main/
│   ├── java/com/example/studentmanagement/
│   │   ├── controller/
│   │   ├── service/
│   │   ├── repository/
│   │   ├── model/
│   │   ├── exception/
│   │   └── StudentManagementApplication.java
│   └── resources/
│       └── application.properties
└── test/
    └── java/com/example/studentmanagement/
```

## Database Configuration

Create the database in MySQL:

```sql
CREATE DATABASE studentdb;
```

Configure `src/main/resources/application.properties` with your local database credentials.

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

Replace `your_password` with your local MySQL password. Never publish your real password.

## REST API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/students` | Retrieve students |
| GET | `/students/{id}` | Retrieve a student by ID |
| POST | `/students` | Add a student |
| PUT | `/students/{id}` | Update a student |
| DELETE | `/students/{id}` | Delete a student |
| GET | `/students/city/{city}` | Search by city |
| GET | `/students/course/{course}` | Search by course |
| GET | `/students/page?page=0&size=5` | Retrieve a page of students |

Verify the endpoints against the actual controller code before relying on them.

## Sample JSON Request

```json
{
  "name": "Sample Student",
  "age": 21,
  "course": "Computer Science",
  "city": "Bengaluru"
}
```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/asujay0405/student-management-system.git
   ```

2. Open the project in your Java IDE.
3. Create the `studentdb` database in MySQL.
4. Configure the database connection in `application.properties`.
5. Run `StudentManagementApplication.java`.
6. Test the endpoints using Postman.

## Future Improvements

- Spring Security and authentication
- Swagger/OpenAPI documentation
- Role-based access control
- Automated unit and integration tests
- Docker support

## Maintainer

**Sujay A.**

- Computer Science Engineering Student
- Java | Spring Boot | MySQL | REST APIs
- GitHub: https://github.com/asujay0405

