Django + PostgreSQL with Docker

A Django REST API for book management, containerized with Docker Compose.

 About This Project
This project demonstrates a complete Django application containerized with Docker. I built this step-by-step while learning Docker containerization and multi-service orchestration.

 What I Built
Django REST API for managing books

PostgreSQL database for data persistence

Docker containerization for both services

Docker Compose for multi-container orchestration

 What I Did (Step by Step)

1. Initial Setup
Created Django project and app

Configured PostgreSQL database connection

Tested locally with virtual environment

2. Docker Configuration
Created Dockerfile for Django application

Created docker-compose.yml for multi-container setup

Configured PostgreSQL service with health checks

3. Final Working Setup
 Both containers running on same network

 Django successfully connected to PostgreSQL

 Database migrations applied automatically

 Application accessible at http://localhost:8000

Technologies Used
Django - Python web framework

PostgreSQL - Database

Docker - Containerization

Docker Compose - Multi-container orchestration


🎯 Key Commands I Used
bash
# Build and run
sudo docker compose up --build

# Stop containers
sudo docker compose down

# Remove everything (including volumes)
sudo docker compose down -v

# Check running containers
sudo docker ps

# View logs
sudo docker logs django_backend