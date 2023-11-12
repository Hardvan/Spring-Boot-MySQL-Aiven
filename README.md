# Spring MySQL Demo Application

This is a simple Spring Boot application demonstrating basic CRUD operations using MySQL as the database. The application includes an entity `User`, a repository `UserRepository`, and a RESTful controller `MainController` exposing endpoints for adding users and retrieving all users.

## Prerequisites

Make sure you have the following installed:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)
- [MySQL](https://www.mysql.com/) database on Aiven (Cloud) or local machine

## Setup

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Configure MySQL on Aiven

## Project Structure

- **DemoApplication.java**: The entry point for the Spring Boot application.
- **User.java**: Entity class representing a user with `id`, `name`, and `email` fields.
- **UserRepository.java**: Interface extending `CrudRepository` for user data access operations.
- **MainController.java**: RESTful controller providing endpoints for adding and retrieving users.

## Running the Application

Run the `DemoApplication.java` class as a Java application.
The application will start on `localhost:8090` (specified in `application.properties`).
You can change the port number in `application.properties` if required.

## Endpoints

- **GET /demo/all**: Retrieve all users.
  ```bash
  curl http://localhost:8080/demo/all
  ```

- **POST /demo/add**: Add a new user. Provide `name` and `email` as request parameters.
  ```bash
  Invoke-WebRequest -Uri http://localhost:8090/demo/add -Method POST -Body @{
    name = "Hardvan"
    email = "123@email.com"
}
  ```

## [YouTube Tutorial Link](https://youtu.be/aS0t9HTO5V4?si=DgGkocBOSg4FxUkQ)
