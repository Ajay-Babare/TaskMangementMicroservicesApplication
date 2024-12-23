# Task Management Microservices Application

Welcome to the **Task Management Microservices Application**! This project implements a task management system using microservices architecture. The application is designed to manage tasks, handle user authentication, and process submissions. It is built using various microservices, each responsible for a specific domain.

## Microservices Overview

### 1. **User Service**
   - The User Service handles user authentication and management. It allows the creation, updating, and deletion of users.
   - Repository: [User Service](https://github.com/Ajay-Babare/Task_User_Service)

### 2. **Task Service**
   - The Task Service is responsible for managing tasks. It supports task creation, assignment, updates, and deletion.
   - Repository: [Task Service](https://github.com/Ajay-Babare/Task_Service)

### 3. **Submission Service**
   - The Submission Service manages the submission of tasks. Users can submit their completed tasks through this service.
   - Repository: [Submission Service](https://github.com/Ajay-Babare/task_submission_service)

### 4. **API Gateway**
   - The API Gateway acts as a single entry point for all microservices. It routes client requests to the appropriate microservice and handles authentication.
   - Repository: [API Gateway](https://github.com/Ajay-Babare/task_api_gateway)

### 5. **Eureka Server**
   - Eureka Server is a service registry that helps with the discovery and registration of microservices in the system.
   - Repository: [Eureka Server](https://github.com/Ajay-Babare/task_eureka_server)

## Technologies Used
- **Spring Boot** for creating RESTful microservices
- **Eureka** for service discovery
- **API Gateway** for routing requests
- **Spring Security** for authentication and authorization
- **MySQL** for database storage


### Steps to Run Locally

Clone the repositories:
   ```bash
   git clone https://github.com/Ajay-Babare/Task_User_Service
   git clone https://github.com/Ajay-Babare/Task_Service
   git clone https://github.com/Ajay-Babare/task_submission_service
   git clone https://github.com/Ajay-Babare/task_api_gateway
   git clone https://github.com/Ajay-Babare/task_eureka_server
