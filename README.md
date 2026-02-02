## CI/CD Pipeline – Jenkins + Docker on AWS EC2

This project implements a CI/CD pipeline using Jenkins and Docker.

Flow:
GitHub -> Jenkins -> Docker Build -> Docker Run (Deploy)

Tools:
- GitHub
- Jenkins
- Docker
- AWS EC2

Pipeline features:
- Triggered automatically using GitHub webhook
- Pipeline defined using Jenkinsfile (Pipeline as Code)
- Builds Docker image
- Deploys container on EC2 instance
