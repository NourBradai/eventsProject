# Events Management Application – CI/CD DevOps Project

This project implements a complete CI/CD pipeline for a Spring Boot events management application.
It was developed as part of a DevOps academic project to demonstrate automation, continuous integration,
continuous deployment, and monitoring practices.

---

## Application Overview

The application is a backend system for managing events, including:
- Event management
- Participants management
- Logistics management

It provides basic CRUD operations and is built using Spring Boot.

---

## Technologies & Tools

### Backend
- Java
- Spring Boot
- Maven
- MySQL

### CI/CD & DevOps
- GitHub (source code management)
- Jenkins (CI/CD automation)
- SonarQube (code quality analysis)
- Nexus Repository (artifact management)
- Docker & Docker Hub (containerization)
- Docker Compose (multi-container orchestration)

### Monitoring
- Prometheus
- Grafana
- cAdvisor

---

## CI/CD Pipeline Overview

The CI/CD pipeline automates the following steps:

1. Source code retrieval from GitHub
2. Compilation and unit tests execution using Maven (JUnit)
3. Code quality analysis using SonarQube
4. Packaging of the Spring Boot application (JAR)
5. Deployment of the artifact to Nexus Repository
6. Docker image build
7. Push of the Docker image to Docker Hub
8. Deployment of the application using Docker Compose
9. Monitoring of containers and application metrics

The pipeline logic is defined in the `Jenkinsfile` located at the root of the repository.

---

## Docker & Deployment

- The application is packaged as a Docker image.
- Docker Compose is used to run:
  - Spring Boot backend
  - MySQL database
  - Monitoring stack (Prometheus, Grafana, cAdvisor)

Environment variables are used to configure database access and application settings.

---

## Testing

- Unit tests are implemented using JUnit and Mockito.
- Functional testing is performed using Swagger UI.

---

## Monitoring

- Prometheus collects metrics from Docker containers and the Spring Boot application.
- Grafana provides dashboards for visualizing CPU, memory usage, and container health.

---

## Notes

- Credentials and sensitive configuration files (e.g., `settings.xml`) are managed locally and are not versioned.
- The Jenkinsfile formalizes the CI/CD pipeline described in the project report.

---
