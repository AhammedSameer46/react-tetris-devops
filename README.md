# React Tetris DevOps Platform

A containerized React Tetris application extended into a complete DevOps and cloud-native deployment project.

This project started from the original open-source React Tetris application and is being transformed into a production-style infrastructure platform using Docker, Kubernetes, GitOps, CI/CD, monitoring, and security tooling.

---

# Original Project

Frontend game originally created by Marcelo Carvalho.

Original repository:
https://github.com/mpirescarvalho/react-tetris

This project extends the original application with DevOps architecture and deployment tooling.

---

# Project Goals

- Containerize a React application using Docker
- Serve production build using NGINX
- Push Docker images to Docker Hub
- Implement CI/CD pipelines using GitHub Actions
- Add security scanning using Trivy and SonarQube
- Deploy application to Kubernetes
- Implement GitOps using ArgoCD
- Add monitoring using Prometheus and Grafana

---

# Tech Stack

## Frontend
- React
- Styled Components

## Containerization
- Docker
- NGINX

## CI/CD
- GitHub Actions

## Security
- Trivy
- SonarQube

## Orchestration
- Kubernetes

## GitOps
- ArgoCD

## Monitoring
- Prometheus
- Grafana

---

# Current Architecture

```text
User
  ↓
NGINX Container
  ↓
React Tetris Application
```

Future architecture:

```text
Developer Push
      ↓
GitHub Actions CI/CD
      ↓
Docker Hub
      ↓
Kubernetes Cluster
      ↓
ArgoCD GitOps
      ↓
Prometheus + Grafana Monitoring
```

---

# Project Structure

```bash
react-tetris/

├── nginx/
│   └── default.conf

├── public/
├── src/
├── assets/

├── Dockerfile
├── .dockerignore
├── .gitignore

├── package.json
├── package-lock.json

└── README.md
```

---

# Docker Setup

## Build Docker Image

```bash
docker build -t react-tetris .
```

## Run Container

```bash
docker run -p 3000:80 react-tetris
```

Application will be available at:

```bash
http://localhost:3000
```

---

# NGINX Configuration

Custom NGINX configuration is added to support React SPA routing.

Location:

```bash
nginx/default.conf
```

---

# Current Progress

- [x] Clone React Tetris application
- [x] Configure Docker environment
- [x] Configure WSL2 and Docker Desktop
- [x] Create multi-stage Docker build
- [x] Configure NGINX container
- [x] Optimize Docker image
- [x] Create custom NGINX routing config
- [x] Clean project structure
- [x] Push project to GitHub

---

# Upcoming Phases

- [ ] Push Docker image to Docker Hub
- [ ] Configure GitHub Actions CI/CD pipeline
- [ ] Add Trivy security scanning
- [ ] Add SonarQube code analysis
- [ ] Deploy application to Kubernetes
- [ ] Configure Kubernetes Services & Deployments
- [ ] Implement ArgoCD GitOps workflow
- [ ] Add Prometheus monitoring
- [ ] Add Grafana dashboards

---

# Future Improvements

- Add backend leaderboard API
- Add PostgreSQL database
- Add authentication
- Add Helm charts
- Add Kubernetes ingress controller
- Add HTTPS/TLS support
- Add autoscaling

---

# Author

Ahammed Sameer

---

# License

This project includes code from the original React Tetris project licensed under the MIT License.
Original copyright belongs to Marcelo Carvalho.