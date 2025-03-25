Kaiburr Task API

This is a REST API built using Java Spring Boot that allows managing "task" objects. It supports CRUD operations, task execution tracking, and shell command execution. The API stores data in MongoDB and provides endpoints for searching, creating, deleting, and executing tasks.

Features

Task Management: Create, read, update, and delete tasks.

Task Execution: Run shell commands associated with tasks.

MongoDB Integration: Store and retrieve task details.

RESTful API: Exposes endpoints for interacting with tasks.

Tech Stack

Java Spring Boot

MongoDB

Docker & Kubernetes (if applicable)

Postman (for API testing)

Installation & Setup

1. Clone the repository

git clone https://github.com/DudekulaSaiMallesh31/kaiburr-1-task.git
cd kaiburr-1-task

2. Configure MongoDB

Ensure MongoDB is running locally or update application.properties with your connection details.

3. Build & Run the Application

mvn clean install
mvn spring-boot:run

4. Test API Endpoints

You can use Postman or curl to test the API endpoints.

API Endpoints

Get All Tasks

curl -X GET "http://localhost:8080/tasks" -H "Content-Type: application/json"

Create a New Task

curl -X POST "http://localhost:8080/tasks" \
-H "Content-Type: application/json" \
-d '{
  "name": "Print Hello",
  "owner": "John Smith",
  "command": "echo Hello World!"
}'

Get a Task by ID

curl -X GET "http://localhost:8080/tasks/{id}" -H "Content-Type: application/json"

Replace {id} with the actual task ID, e.g., 67e1901e1b5da9651f29e42c.

Search Tasks by Name

curl -X GET "http://localhost:8080/tasks/search?name=Print" -H "Content-Type: application/json"

Execute a Task

curl -X PUT "http://localhost:8080/tasks/{id}/execute" -H "Content-Type: application/json"

Replace {id} with the real task ID, e.g., http://localhost:8080/tasks/67e1901e1b5da9651f29e42c/execute.

Delete a Task

curl -X DELETE "http://localhost:8080/tasks/{id}" -H "Content-Type: application/json"

Replace {id} with the actual task ID.

Future Enhancements

Add authentication and authorization.

Implement task scheduling.

Improve error handling and logging.

Contributing

Feel free to submit issues or pull requests. Contributions are welcome!

License

This project is open-source and available under the MIT License.

