# React Tetris - DevOps Project

A containerized React Tetris application deployed using Docker and NGINX.

This project is being extended into a full DevOps pipeline with CI/CD, Kubernetes, GitOps, security scanning, and monitoring integrations.

---

# Project Goals

- Containerize a React application using Docker
- Serve production build using NGINX
- Push Docker images to Docker Hub
- Implement CI/CD pipelines using GitHub Actions
- Add security scanning using Trivy and SonarQube
- Deploy application to Kubernetes
- Implement GitOps using ArgoCD
- Monitor infrastructure using Prometheus and Grafana

---

# Tech Stack

- React
- Docker
- NGINX
- GitHub Actions
- Kubernetes
- ArgoCD
- Prometheus
- Grafana
- Trivy
- SonarQube

---

# Project Structure

```bash
react-tetris/

├── nginx/
│   └── default.conf

├── public/
├── src/

├── Dockerfile
├── .dockerignore
├── .gitignore
├── package.json
├── README.md