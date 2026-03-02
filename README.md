# Django + PostgreSQL with Docker

## 1. Introduction
This project demonstrates a Django REST API for managing books, containerized using Docker and orchestrated with Docker Compose. The goal of this project is to understand how a Django application and a PostgreSQL database can run as separate containers while communicating over a shared Docker network.

## 2. About the Project
This project was built while learning Docker containerization and multi-service orchestration. It shows how a backend application and a database service can be deployed together using Docker Compose.

The application allows users to manage book records using a Django REST API while storing the data in a PostgreSQL database.

## 3. Features
- Django REST API for managing books
- PostgreSQL database for persistent data storage
- Docker containerization for the backend service
- Docker Compose for running multiple services
- Automatic database migrations
- Communication between containers through a shared Docker network

## 4. Project Components

### 4.1 Backend Service
The backend service runs the Django application. It handles API requests and communicates with the PostgreSQL database to store and retrieve data.

### 4.2 Database Service
The PostgreSQL service stores all the application data. Docker volumes are used to ensure that the data persists even if the container stops.

## 5. Implementation Steps

### 5.1 Initial Setup
- Created a Django project
- Created a Django app for managing books
- Configured PostgreSQL database connection
- Tested the application locally using a Python virtual environment

### 5.2 Docker Configuration
- Created a Dockerfile for the Django application
- Created a docker-compose.yml file for running multiple containers
- Configured a PostgreSQL service with environment variables and persistent volumes

### 5.3 Final Working Setup
- Both containers run on the same Docker network
- Django successfully connects to PostgreSQL
- Database migrations run successfully
- Application is accessible at http://localhost:8000

## 6. Technologies Used
- Django – Python web framework
- PostgreSQL – Relational database system
- Docker – Containerization platform
- Docker Compose – Multi-container orchestration tool

## 7. Important Docker Commands

### Build and run the containers
sudo docker compose up --build


### Stop running containers

sudo docker compose down


### Remove containers and volumes

sudo docker compose down -v


### Check running containers

sudo docker ps


### View container logs

sudo docker logs django_backend


## 8. Conclusion
This project demonstrates how a Django backend and PostgreSQL database can be containerized and deployed using Docker Compose. It provides a simple example of multi-container architecture commonly used in modern backend development.