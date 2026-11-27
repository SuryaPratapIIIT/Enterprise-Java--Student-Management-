# Student Management System

## Overview

The Student Management System is a Java-based backend application developed with Spring Boot. It provides RESTful APIs to store, access, and manage student information along with their enrolled courses.

The project demonstrates backend development concepts such as REST API development, database connectivity, entity relationships, and authentication.

## Key Functionalities

- Add new student records.
- Retrieve student details using their ID.
- Store student information in a MySQL database.
- Maintain relationships between students and courses.
- Automatically generate student and course IDs.
- Validate incoming student data.
- Secure API endpoints using Spring Security.

## Technologies Used

- **Java** – Core programming language
- **Spring Boot** – Backend application development
- **Spring Data JPA** – Object-relational mapping and database access
- **Spring Security** – API authentication
- **MySQL** – Data storage
- **Maven** – Project and dependency management

## Application Architecture

The application follows a layered architecture:

1. **Controller Layer:** Handles incoming HTTP requests.
2. **Service Layer:** Contains application business logic.
3. **Repository Layer:** Communicates with the database.
4. **Entity Layer:** Defines Student and Course database entities.
5. **Configuration Layer:** Contains application security configuration.

## Database Design

The application uses two main entities:

### Student
- ID
- Name
- Email

### Course
- ID
- Course Name
- Credits
- Student ID

**Relationship:** One student can be associated with multiple courses. This is implemented using a One-to-Many relationship in JPA.

## Getting Started

### Prerequisites

- Java Development Kit
- MySQL Server
- Maven
- An IDE such as IntelliJ IDEA or VS Code

### Installation

**1. Clone the repository**

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd student-management
```

**2. Create the database**

```sql
CREATE DATABASE studentdb;
```

**3. Configure environment variables**

Set these variables in your system:

```text
DB_USERNAME=your_mysql_username
DB_PASSWORD=your_mysql_password
APP_USERNAME=your_application_username
APP_PASSWORD=your_application_password
```

**4. Start the application**

```bash
mvn spring-boot:run
```

The server runs on port `8081`.

## API Reference

| HTTP Method | Endpoint | Function |
|---|---|---|
| GET | `/hello` | Checks application availability |
| GET | `/students/{id}` | Fetches student information |
| POST | `/students` | Registers a new student |

### Sample POST Request

Endpoint:

```text
POST http://localhost:8081/students
```

JSON Body:

```json
{
  "name": "Rahul Sharma",
  "email": "rahul@example.com"
}
```

## Security

Spring Security is configured with HTTP Basic Authentication.

- The `/hello` GET endpoint is publicly accessible.
- Other endpoints require authentication.
- Credentials are configured through environment variables rather than committed to the repository.

## Learning Outcomes

Through this project, the following concepts were explored:

- Building RESTful web services.
- Working with Spring Boot and Spring Data JPA.
- Connecting Java applications to MySQL.
- Implementing entity relationships.
- Configuring authentication and authorization.
- Testing APIs using HTTP requests.

## Future Scope

- Implement complete CRUD operations.
- Add course management endpoints.
- Introduce pagination and sorting.
- Improve API exception handling.
- Integrate Swagger for API documentation.

## Conclusion

This project provides practical experience in Java backend development and serves as a foundation for building larger database-driven applications.
