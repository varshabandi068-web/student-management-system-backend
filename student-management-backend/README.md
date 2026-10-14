# Student Management System — Spring Boot Backend

## Requirements
- Java JDK 21
- Maven 3.9+ (or open this folder as a Maven project in IntelliJ IDEA)
- MySQL Server

## 1. Configure MySQL
Open `src/main/resources/application.properties` and replace `YOUR_MYSQL_PASSWORD` with your MySQL password. The configured database is `studentdb`; `createDatabaseIfNotExist=true` creates it when permissions allow.

If you prefer creating it manually in MySQL:
```sql
CREATE DATABASE studentdb;
```
The application creates/updates the `students` table automatically using JPA.

## 2. Run the backend
Open a terminal in this folder and run:
```bash
mvn spring-boot:run
```
If `mvn` is not recognized on Windows, install Apache Maven and add its `bin` folder to PATH, or open this folder in IntelliJ IDEA and run `StudentManagementApplication.java`.

Backend URL: `http://localhost:8080`
API base URL: `http://localhost:8080/api/students`

## API endpoints
- `GET /api/students` — list students
- `GET /api/students/{id}` — get one student
- `POST /api/students` — create student
- `PUT /api/students/{id}` — update student
- `DELETE /api/students/{id}` — delete student

Example JSON:
```json
{
  "name": "Varsha",
  "rollNumber": "CSE001",
  "email": "varsha@example.com",
  "phone": "9876543210",
  "department": "CSE",
  "year": 3
}
```
