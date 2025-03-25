# Task1_Kaiburr
This is a Java Spring Boot REST API for managing and executing shell command tasks in a Kubernetes pod. The tasks are stored in a MongoDB database.
# Task Manager API

This is a Java Spring Boot REST API for managing and executing shell command tasks in a Kubernetes pod. The tasks are stored in a MongoDB database.

## Features
- **Create Tasks**: Add new tasks with an ID, name, owner, and command.
- **Get Tasks**: Retrieve all tasks or a specific task by ID.
- **Delete Tasks**: Remove tasks by ID.
- **Find Tasks by Name**: Search tasks based on partial name matches.
- **Execute Tasks**: Run the shell command associated with a task and store execution details.

## Installation & Setup
### Prerequisites
- Java 17+
- MongoDB
- Maven

### Clone Repository
```sh
git clone https://github.com/your-username/task-manager-api.git
cd task-manager-api
```

### Build and Run
```sh
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

## API Endpoints
### Get all tasks
```sh
GET /tasks
```
### Get task by ID
```sh
GET /tasks?id={taskId}
```
### Create a new task
```sh
PUT /tasks
Content-Type: application/json
{
  "id": "123",
  "name": "Print Hello",
  "owner": "John Smith",
  "command": "echo Hello World!"
}
```
### Delete a task
```sh
DELETE /tasks/{id}
```
### Find tasks by name
```sh
GET /tasks/find?name=Print
```
### Execute a task
```sh
PUT /tasks/{id}/execute
```

## Testing
Use **Postman**, **cURL**, or any HTTP client to interact with the API.

Example using `curl`:
```sh
curl -X GET "http://localhost:8080/tasks"
```

