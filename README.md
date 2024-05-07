# SchoolApp

## Introduction
SchoolApp is a web-based application developed using the Jakarta Servlet technology, designed to manage teacher data within a school setting. This application facilitates operations such as adding, updating, deleting, and searching for teachers through a user-friendly interface. It also implements authentication and session management to ensure that only authorized users can access the system.

## Features
- **Teacher Management**: Allows users to add, update, and delete teacher records in the database.
- **Authentication System**: Manages user login sessions with secure password handling.
- **Search Functionality**: Users can search for teachers by their last names.
- **Data Integrity**: Includes functionality to reset the database while maintaining foreign key constraints.
- **Security**: Implements filters to manage UTF-8 encoding and session-based user authentication.

## Technology Stack
- **Jakarta Servlets**: Core technology for handling requests and responses.
- **JSP**: JavaServer Pages for dynamic web content.
- **MySQL**: Backend database to store all application data.
- **BCrypt**: For hashing user passwords securely.
- **Apache Commons DBCP**: For efficient database connection pooling.
- **JDBC**: Java Database Connectivity for database interactions.

## Setup and Installation
### Prerequisites
- Java JDK 11 or later.
- Apache Tomcat 9 or later.
- MySQL Server 5.7 or later.
- An IDE such as IntelliJ IDEA or Eclipse.

### Database Configuration
- Create a database named `schooldb`.
- Import the SQL schema and initial data (provided separately).
- Configure environment variables for database access:
  - `DB_URL`: URL to your database.
  - `DB_USER`: Database username.
  - `DB_PASSWORD`: Database password.

### Building the Project
- Clone the repository to your local machine.
- Open the project in your IDE and resolve dependencies.
- Build the project to generate a `.war` file.

### Deploying the Application
- Copy the `.war` file into your Tomcat's `webapps` directory.
- Start the Tomcat server.

### Accessing the Application
- Open a web browser.
- Navigate to `http://localhost:8080/SchoolApp` to access the application.

## Architectural Overview
- **Data Access Object (DAO)**: Handles all database interactions.
- **Data Transfer Object (DTO)**: Used to transfer data between layers.
- **Service Layer**: Provides business logic and transaction management.
- **Controller**: Handles HTTP requests, invokes business logic, and manages responses.
- **Filter**: Ensures encoding and authentication across the application.
- **Model**: Represents the data structure.
- **Security Utilities**: Provides password hashing and validation.

## Important Classes and Interfaces
- `TeacherDAOImpl`: Implements CRUD operations for teacher entities.
- `AuthenticationProvider`: Manages user authentication.
- `TeacherService`: Implements business logic for teacher operations.
- `LoginController`, `DeleteTeacherController`, `InsertTeacherController`: Servlets handling respective web operations.

## Contributors
- Tsakiris Filippos

## License
There is no formal license for this project. Everyone can use it freely.
