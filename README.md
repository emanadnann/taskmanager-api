# Task Manager API

A RESTful API for managing tasks, built with Java and Spring Boot. Supports full CRUD operations (Create, Read, Update, Delete), backed by a database using Spring Data JPA and H2.

## Features

- Create new tasks
- Retrieve all tasks or a single task by ID
- Update existing tasks
- Delete tasks
- Data persisted using Spring Data JPA with an H2 database

## Tech Stack

- **Java 17**
- **Spring Boot** (Spring Web, Spring Data JPA)
- **H2 Database** (in-memory)
- **Maven** (build tool)

## Getting Started

### Prerequisites

- Java 17 or later installed
- Maven (or use the included `mvnw` wrapper)

### Running the project

```bash
./mvnw spring-boot:run
```

The API will start on `http://localhost:8080`.

## API Endpoints

| Method | Endpoint       | Description              |
|--------|----------------|---------------------------|
| GET    | `/tasks`       | Get all tasks             |
| GET    | `/tasks/{id}`  | Get a single task by ID   |
| POST   | `/tasks`       | Create a new task         |
| PUT    | `/tasks/{id}`  | Update an existing task   |
| DELETE | `/tasks/{id}`  | Delete a task              |

### Example request body (POST / PUT)

```json
{
    "title": "Finish project setup",
    "description": "Complete the Spring Boot task manager",
    "status": "in progress"
}
```

## Project Structure

- `Task.java` — the entity representing a task, mapped to a database table
- `TaskRepository.java` — the interface providing database access (via Spring Data JPA)
- `TaskController.java` — the REST controller exposing the API endpoints

## What I learned

Building this project helped me understand how REST APIs work in practice — handling HTTP requests, mapping data to a database using JPA, and structuring an application with a clear separation between the entity, repository, and controller layers.
