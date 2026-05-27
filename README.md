# React Tetris DevOps Platform

A cloud-native DevOps project built around the open-source React Tetris application.

This project demonstrates a complete DevOps workflow including containerization, CI/CD automation, Kubernetes orchestration, GitOps deployment, security scanning, and monitoring.

---

# Original Project

Frontend game originally created by Marcelo Carvalho.

Original Repository:

https://github.com/mpirescarvalho/react-tetris

This repository extends the original application by implementing production-grade DevOps practices and cloud-native tooling.

---

# Project Overview

The goal of this project is to simulate a real-world DevOps workflow used in modern software engineering teams.

The application is:

- Containerized using Docker
- Served using NGINX
- Published to Docker Hub
- Built automatically using GitHub Actions
- Security scanned using Trivy
- Deployed to Kubernetes
- Managed with Helm
- Continuously synchronized using ArgoCD
- Monitored using Prometheus
- Visualized using Grafana

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

## Orchestration

- Kubernetes

## Package Management

- Helm

## GitOps

- ArgoCD

## Monitoring

- Prometheus
- Grafana

---

# DevOps Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions CI/CD
    │
    ▼
Trivy Security Scan
    │
    ▼
Docker Hub
    │
    ▼
ArgoCD
    │
    ▼
Kubernetes Cluster
    │
    ▼
React Tetris Deployment
    │
    ▼
Prometheus
    │
    ▼
Grafana Dashboard
```

---

# Project Structure

```text
react-tetris/

├── .github/
│   └── workflows/
│       └── docker-build.yml
│
├── helm/
│   └── react-tetris/
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates/
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
│
├── nginx/
│   └── default.conf
│
├── public/
├── src/
├── assets/
│
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

Application:

```text
http://localhost:3000
```

---

# Docker Hub

Production image is published to Docker Hub.

Repository:

```text
ahammed46/react-tetris-devops
```

Pull image:

```bash
docker pull ahammed46/react-tetris-devops:v1
```

---

# CI/CD Pipeline

GitHub Actions automates:

- Source code checkout
- Docker image build
- Docker Hub authentication
- Trivy security scanning
- Docker image push

Workflow location:

```text
.github/workflows/docker-build.yml
```

---

# Security Scanning

Trivy is integrated into the CI/CD pipeline.

The pipeline automatically scans:

- Operating system packages
- Application dependencies
- Critical vulnerabilities
- High-severity vulnerabilities

This helps identify security risks before deployment.

---

# Kubernetes Deployment

The application is deployed to Kubernetes using:

- Deployment
- Service
- Replica Sets
- Pods

Features:

- Replica-based scaling
- Self-healing pods
- Declarative infrastructure

Example:

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

---

# Helm Deployment

The Kubernetes manifests were converted into a reusable Helm chart.

Benefits:

- Reusable deployments
- Versioned releases
- Easier upgrades
- Environment-specific configurations

Install:

```bash
helm install react-tetris ./react-tetris
```

Check release:

```bash
helm list
```

---

# GitOps with ArgoCD

ArgoCD continuously monitors the GitHub repository and synchronizes Kubernetes resources automatically.

Features:

- Git as the single source of truth
- Continuous deployment
- Deployment history
- Rollback support
- Automated synchronization

---

# Monitoring Stack

## Prometheus

Prometheus collects:

- Kubernetes metrics
- Node metrics
- Pod metrics
- Cluster metrics

Example query:

```text
up
```

---

## Grafana

Grafana visualizes:

- CPU Usage
- Memory Usage
- Network Usage
- Cluster Health

through customizable dashboards.

---

# Project Progress

## Phase 1 — Docker Containerization

- [x] Multi-stage Docker build
- [x] NGINX production configuration
- [x] Docker image optimization

## Phase 2 — Docker Hub

- [x] Publish image to Docker Hub

## Phase 3 — CI/CD

- [x] GitHub Actions pipeline
- [x] Automated Docker builds

## Phase 4 — Security

- [x] Trivy vulnerability scanning

## Phase 5 — Kubernetes

- [x] Deployment manifest
- [x] Service manifest
- [x] Replica management
- [x] Self-healing validation

## Phase 6 — Helm

- [x] Helm chart creation
- [x] Helm deployment

## Phase 7 — GitOps

- [x] ArgoCD installation
- [x] Git synchronization
- [x] Continuous deployment

## Phase 8 — Monitoring

- [x] Prometheus installation
- [x] Grafana integration
- [x] Dashboard creation

---

# Screenshots

## Docker Hub Repository

![Docker Hub](screenshots/dockerhub.png)

---

## ArgoCD GitOps Dashboard

![ArgoCD](screenshots/argocd.png)

---

## Prometheus Metrics

![Prometheus](screenshots/prometheus.png)

---

## Grafana Dashboard

![Grafana](screenshots/grafana.png)

---

# Key DevOps Features

- Docker Containerization
- Multi-Stage Docker Builds
- NGINX Reverse Proxy
- GitHub Actions CI/CD
- Trivy Security Scanning
- Kubernetes Deployment
- Helm Package Management
- ArgoCD GitOps
- Prometheus Monitoring
- Grafana Visualization

---

# Future Improvements

- SonarQube Integration
- Kubernetes Ingress Controller
- HTTPS/TLS Support
- Horizontal Pod Autoscaler (HPA)
- Backend Leaderboard API
- PostgreSQL Database
- Authentication System
- Multi-Environment Deployments

---

# Learning Outcomes

Through this project I gained hands-on experience with:

- Docker Containerization
- CI/CD Automation
- Kubernetes Administration
- Helm Chart Development
- GitOps Workflows
- Infrastructure as Code
- Monitoring and Observability
- Security Scanning
- Production Deployment Practices

---

# Author

**Ahammed Sameer**

GitHub:

https://github.com/AhammedSameer46

LinkedIn:

https://www.linkedin.com/in/ahammed-sameer-28b3a2390/

---

# License

This project includes code from the original React Tetris project licensed under the MIT License.

Original copyright belongs to Marcelo Carvalho.