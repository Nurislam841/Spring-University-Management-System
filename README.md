# University Management System (Spring Boot)

A backend University Management System built with **Spring Boot**, designed to manage students, courses, instructors, and enrollments using a clean layered architecture.

This project demonstrates REST API development, role-based security, and database integration using modern Java technologies.

---

## Overview

The system allows administrators to:

- Manage students
- Manage instructors
- Create and manage courses
- Handle student enrollments
- Secure endpoints with authentication & authorization

The application follows a standard Spring Boot layered structure:

Controller → Service → Repository → Entity

---

## Tech Stack

Backend:
- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Security
- Hibernate

Database:
- PostgreSQL / MySQL / H2 (update based on your setup)

Security:
- Spring Security
- JWT Authentication (if implemented)
- Password hashing with BCrypt

Build Tool:
- Maven

---

## Project Structure

```

src/main/java/com/yourpackage/
│
├── controller/        # REST Controllers
├── service/           # Business logic
├── repository/        # JPA Repositories
├── entity/            # Database Entities
├── dto/               # Data Transfer Objects (if used)
├── config/            # Security & configuration
└── UniversityManagementApplication.java

````

---

## Features

### Authentication & Security
- User registration
- Login authentication
- Password encryption (BCrypt)
- Role-based access control (ADMIN / INSTRUCTOR / STUDENT)
- Protected API endpoints

### Student Management
- Create student
- Update student
- Delete student
- View student details
- Enroll student in courses

### Course Management
- Create course
- Update course
- Delete course
- Assign instructor
- View enrolled students

### Instructor Management
- Create instructor
- Assign courses
- View teaching courses

---

## Installation

### 1. Clone repository

```bash
git clone https://github.com/your-username/university-management-system.git
cd university-management-system
````

### 2. Configure Database

Edit `application.properties` or `application.yml`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/university_db
spring.datasource.username=postgres
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

server.port=8080
```

Adjust for MySQL or H2 if needed.

---

### 3. Build project

```bash
mvn clean install
```

---

### 4. Run application

```bash
mvn spring-boot:run
```

Or run the generated JAR:

```bash
java -jar target/university-management-system-0.0.1-SNAPSHOT.jar
```

Application will run on:

```
http://localhost:8080
```

---

## API Endpoints (Example)

### Authentication

```
POST   /api/auth/register
POST   /api/auth/login
```

### Students

```
GET    /api/students
GET    /api/students/{id}
POST   /api/students
PUT    /api/students/{id}
DELETE /api/students/{id}
```

### Courses

```
GET    /api/courses
POST   /api/courses
PUT    /api/courses/{id}
DELETE /api/courses/{id}
```

---

## Testing

Run tests with:

```bash
mvn test
```

---

## Learning Objectives

* Build REST APIs using Spring Boot
* Implement layered architecture
* Integrate relational databases using JPA
* Apply authentication & authorization
* Work with real-world backend structure

---

## Author

Baltabekov Nurislam

Software Engineering Student

Backend Developer (Java / Spring Boot)

---

## License

This project is developed for educational purposes.
