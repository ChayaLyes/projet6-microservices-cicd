# Projet 6 — Pipeline CI/CD pour Microservices

## Description
Pipeline CI/CD complet pour une architecture microservices deployee sur Kubernetes k3s.

## Architecture
Developer → GitHub → GitLab CI/CD
→ Maven Build → Docker Build
→ Docker Hub → Helm → k3s

## Microservices
- api-service (port 8080) : API principale
- auth-service (port 8081) : Authentification JWT
- PostgreSQL (port 5432) : Base de donnees

## Stack Technique
- CI/CD : GitLab CI
- Build : Maven + Java 17
- Conteneur : Docker
- Registry : Docker Hub
- Orchestration : Kubernetes k3s
- Packaging : Helm Charts
- Tests : Newman Postman
- Monitoring : Prometheus + Grafana

## Structure
projet6-microservices-cicd/
├── services/
│   ├── api-service/
│   ├── auth-service/
│   └── frontend/
├── helm/
│   ├── api-service/
│   ├── auth-service/
│   └── postgresql/
├── k8s/
└── .gitlab-ci.yml
