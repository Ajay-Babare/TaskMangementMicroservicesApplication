# Task Management Microservices Application

Welcome to the **Task Management Microservices Application**! This system is designed to efficiently manage tasks, handle user authentication, and process submissions using microservices architecture. It is built with a collection of services, each responsible for a specific domain, ensuring scalability, flexibility, and maintainability.

---
## Features
- **User Service**: Handles user authentication and user-related operations (create, update, delete).
- **Task Service**: Manages tasks, including task creation, assignment, updates, and deletion.
- **Submission Service**: Manages task submissions where users can submit their completed tasks.
- **API Gateway**: Single entry point for routing client requests to the appropriate microservice and handling authentication.
- **Eureka Server**: Service registry that provides service discovery and enables dynamic communication between microservices.

---
## Architecture
The application follows the **Microservices Architecture** pattern with the following core components:

- **User Service**: Handles user management (authentication, CRUD operations).
- **Task Service**: Manages tasks lifecycle (create, assign, update, delete).
- **Submission Service**: Manages task submission operations.
- **API Gateway**: Acts as a reverse proxy to route requests to the appropriate microservice and manage authentication.
- **Eureka Server**: Service registry for service discovery, enabling microservices to locate each other.

---
## Technologies Used
- **Spring Boot**: For creating RESTful microservices.
- **Spring Cloud Eureka**: For service discovery and registration.
- **Spring Security**: For authentication and authorization.
- **MySQL**: For database storage.
- **Spring Cloud Gateway**: For routing requests and acting as an API Gateway.
- **Docker (optional)**: For containerization of services.

---
## Microservices Breakdown
### 1. User Service
Responsible for managing users, including registration, login, and user profile updates.

#### Operations:
- Create user
- Update user
- Delete user
- Authenticate user


- **Repository**: [User Service Repository](https://github.com/Ajay-Babare/Task_User_Service)

### 2. Task Service
Responsible for managing the lifecycle of tasks.

#### Operations:

- Create task
- Update task
- Delete task
- Assign task to users


- **Repository**: [Task Service Repository](https://github.com/Ajay-Babare/Task_Service)

### 3. Submission Service
Handles the submission of tasks by users.

#### Operations:

- Submit completed task
- Track task submission status
- **Repository**: [Submission Service Repository](https://github.com/Ajay-Babare/task_submission_service)

### 4. API Gateway
Acts as a single entry point for routing client requests to the appropriate microservices and managing authentication.

**Repository**: [API Gateway Repository](https://github.com/Ajay-Babare/task_api_gateway)

### 5. Eureka Server
A service registry that helps microservices discover each other dynamically.

**Repository**: [Eureka Server Repository](https://github.com/Ajay-Babare/task_eureka_server)

---
### Local Setup
To run this application locally, follow the steps below:

##### Prerequisites:
JDK 11+ (recommended version)
MySQL Database setup
Maven or Gradle (for building the application)
Docker (optional)

#### Steps:
Clone the Repositories: Clone all the necessary microservice repositories to your local machine:

<pre>
    git clone https://github.com/Ajay-Babare/Task_User_Service
    git clone https://github.com/Ajay-Babare/Task_Service
    git clone https://github.com/Ajay-Babare/task_submission_service
    git clone https://github.com/Ajay-Babare/task_api_gateway
    git clone https://github.com/Ajay-Babare/task_eureka_server
</pre>

### Set up the Database:

- Ensure that MySQL is installed and running on your local machine.
- Create the required databases and tables based on the schema provided in each service's repository (if applicable).

### Configure Application Properties:

- Update the database connection details in application.properties or application.yml in each microservice to match your local database setup.
- For the API Gateway, configure it to route requests correctly.

### Run the Services:

- Run the Eureka Server first to start the service registry.
- Start the User Service, Task Service, Submission Service, and API Gateway sequentially.
Example (using Spring Boot’s built-in Maven plugin):

```bash
cd task_eureka_server
mvn spring-boot:run

cd ../task_api_gateway
mvn spring-boot:run

cd ../Task_User_Service
mvn spring-boot:run

cd ../Task_Service
mvn spring-boot:run

cd ../task_submission_service
mvn spring-boot:run
```
### Access the Application: 
Once all services are running, you can access the API Gateway at `http://localhost:8080`. This is the entry point for all client requests.

---
### Testing:

- You can use Postman or any other API testing tool to test the endpoints.
- The API Gateway will route the requests to the correct microservice.

---
#### API Documentation

##### Authentication API (User Service)
- **POST /auth/register**: Register a new user.
- **POST /auth/login**: Login and receive a JWT token.

##### Task Management API (Task Service)
- **POST /tasks**: Create a new task.
- **PUT /tasks/{id}**: Update a task.
- **DELETE /tasks/{id}**: Delete a task.

##### Task Submission API (Submission Service)
- **POST /submissions**: Submit a completed task.
- **GET /submissions/{taskId}**: Get the status of a task submission.

---
### Contributing
We welcome contributions to improve the functionality of this application. Please follow these steps to contribute:

1. Fork the repository.
2. Create a feature branch (git checkout -b feature-name).
3. Commit your changes (git commit -am 'Add new feature').
4. Push the branch (git push origin feature-name).
5. Create a new Pull Request.

---
### License
This project is licensed under the MIT License – see the LICENSE file for details.
