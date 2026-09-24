# Hope Medical Center

Hope Medical Center is a healthcare management web application designed to make patient registration and appointment booking easier, faster, and more organized. The project combines a modern frontend, a secure Flask backend, and a MySQL database, and is deployed using Docker Compose and Kubernetes manifests.

---

## Problem Statement

Healthcare systems often struggle with:

- Manual appointment scheduling and long waiting times
- Lack of a centralized digital platform for patient registration
- Difficulty in managing patient details and appointment information securely
- Limited scalability when the application needs to run in different environments
- Slow deployment and setup for teams using different infrastructure tools

This project addresses those issues by creating a simple but effective medical web application where patients can:

- register an account
- log in securely
- book an appointment
- choose a department
- submit details such as time, phone number, and notes

At the same time, the backend stores all this information in a MySQL database, making the system more organized and reliable.

---

## What I Built

I created a full-stack medical booking system with:

- Frontend website for Hope Medical Center
- Patient registration and login support
- Appointment booking form
- Flask REST API for backend processing
- MySQL database for structured data storage
- Docker Compose setup for local deployment
- Kubernetes YAML files for cloud-native deployment

This project is not just a simple landing page; it is a working system that demonstrates real-world software deployment and architecture patterns.

---

## Project Overview

### Tech Stack

- Frontend: HTML, CSS, JavaScript
- Backend: Python, Flask
- Database: MySQL
- Containerization: Docker, Docker Compose
- Orchestration: Kubernetes (YAML manifests)
- Hosting/Runtime: Nginx for frontend serving

### Core Features

- Modern healthcare landing page
- About page and service information
- Doctor and specialty sections
- Patient registration form
- Secure user password hashing
- Appointment booking API
- MySQL-backed persistence
- Dockerized deployment
- Kubernetes-ready architecture

---

## Project Structure

```bash
hope-medical-center-docker-k8s/
├── backend/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
├── frontend/
│   ├── about.html
│   ├── code.js
│   ├── Dockerfile
│   ├── index.html
│   ├── nginx.conf
│   ├── register.html
│   └── style.css
├── architecture/
├── Screenshots/
├── backend-k8s.yaml
├── backend-deployment.yaml
├── docker-compose.yml
├── frontend-k8s.yaml
├── ingress.yaml
├── mysql-deployment.yaml
├── mysql-pvc.yaml
├── mysql-service.yaml
└── README.md
```

---

## Application Flow

1. Users open the hospital website.
2. They can register or log in to the system.
3. Patients book an appointment by filling the form.
4. The frontend sends data to the Flask backend.
5. The backend validates and saves the details into MySQL.
6. The application can be run locally with Docker or deployed to a Kubernetes cluster.

---

## Local Development Setup

### Prerequisites

- Docker
- Docker Compose
- Git
- Optional: Kubernetes tools such as kubectl and minikube

### Run with Docker Compose

From the project root, run:

```bash
docker-compose up --build
```

Then open:

- Frontend: http://localhost:8080
- Backend API: http://localhost:5000
- MySQL: localhost:3307

### Stop the containers

```bash
docker-compose down
```

---

## Docker Configuration

The project uses separate containers for:

- MySQL database
- Flask backend
- Frontend Nginx service

This allows the system to be easily deployed, scaled, and maintained in isolated environments.

---

## Kubernetes Deployment

The project also includes Kubernetes YAML files for deploying the backend and related services. These files define:

- ConfigMaps and Secrets
- Deployments
- Services
- Ingress configuration
- Persistent volume for MySQL data
- Horizontal Pod Autoscaling for backend scaling

### Example deployment step

```bash
kubectl apply -f mysql-pvc.yaml
kubectl apply -f mysql-deployment.yaml
kubectl apply -f mysql-service.yaml
kubectl apply -f backend-k8s.yaml
kubectl apply -f frontend-k8s.yaml
kubectl apply -f ingress.yaml
```

This helps demonstrate how the application can run in a production-like Kubernetes environment.

---

## My Contribution

I implemented the following in this project:

- Designed and built the hospital website frontend
- Added a patient appointment booking workflow
- Connected the frontend with a Python backend API
- Implemented secure user registration and password hashing
- Structured the backend to work with MySQL
- Organized Docker and Kubernetes deployment files
- Made the project ready for containerized and cloud deployment

This project is a strong example of combining frontend development, backend logic, database design, and DevOps deployment practices in one application.

---

## Why This Project Matters

This application reflects a realistic healthcare scenario where digital infrastructure is essential for:

- improving patient experience
- reducing manual work
- ensuring organized appointment management
- supporting future growth and scaling

It also demonstrates how modern cloud-based software can be built with an architecture that is easy to maintain and deploy.

---

## Future Improvements

Some ideas for extending the project:

- patient dashboard
- admin panel for viewing appointments
- email notifications for bookings
- doctor availability calendar
- JWT-based authentication
- role-based access control
- cloud deployment on AWS, Azure, or GCP
- CI/CD pipeline setup

---

## Notes

This project was created as a practical full-stack application for healthcare service management and to demonstrate Docker and Kubernetes deployment workflow. It can be used as a starting point for more advanced medical software systems.

---

## License

This project is intended for learning and demonstration purposes.
