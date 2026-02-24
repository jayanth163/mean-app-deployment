# 🚀 MEAN Stack Application Deployment on Azure

## 📌 Project Overview

This project demonstrates containerization and deployment of a full-stack MEAN (MongoDB, Express, Angular, Node.js) application using Docker, Docker Compose, Nginx, and GitHub Actions CI/CD pipeline on Microsoft Azure.

---

## 🏗 Architecture

GitHub → GitHub Actions → Docker Hub → Azure VM → Docker Compose → Nginx → Application

---

## 🧰 Technologies Used

- Node.js
- Express.js
- Angular
- MongoDB
- Docker
- Docker Compose
- Nginx
- GitHub Actions
- Microsoft Azure

---

# 📦 Repository Setup

1. Extracted the provided MEAN application.
2. Created a new GitHub repository.
3. Pushed frontend and backend code.
4. Added Dockerfiles and docker-compose.yml.

---

# 🐳 Dockerization

## Backend Dockerfile

Located at:
backend/Dockerfile

## Frontend Dockerfile

Located at:
frontend/Dockerfile

---

# 🐳 Docker Compose

The docker-compose.yml file orchestrates:

- MongoDB container
- Backend container
- Frontend container

To run locally:
