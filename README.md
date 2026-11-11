
# DevOps CI/CD Project

## Project Overview

This project demonstrates a basic CI/CD pipeline using Jenkins, Docker, and GitHub.

A simple HTML website is stored in GitHub. Jenkins retrieves the source code, builds a Docker image, and deploys the application inside a Docker container.

## Technologies Used

- Git and GitHub – Source code management
- Jenkins – CI/CD pipeline automation
- Docker – Application containerization
- Nginx – Web server
- Ubuntu (WSL) – Development environment

## Project Architecture

GitHub Repository → Jenkins Pipeline → Docker Image → Docker Container → Web Application

## Project Structure

```text
devops-project/
├── index.html
├── Dockerfile
├── Jenkinsfile
└── README.md
```

## Pipeline Stages

### 1. Checkout from GitHub
Jenkins retrieves the latest source code from the GitHub repository.

### 2. Build Docker Image
Jenkins builds a Docker image using the Dockerfile.

### 3. Deploy Application
Jenkins stops and removes the previous project container, then starts a new container using the updated image.

## How to Access the Application

After successful deployment, open:

http://localhost:8080

## Jenkins Dashboard

http://localhost:8081

## How to Run the Project Manually

Build the Docker image:

```bash
docker build -t my-devops-app .
```

Run the container:

```bash
docker run -d --name my-devops-container -p 8080:80 my-devops-app
```

## Learning Outcomes

- Created a Docker image for a web application.
- Integrated GitHub with Jenkins.
- Created a Jenkins pipeline using a Jenkinsfile.
- Configured Jenkins to execute Docker commands.
- Built and deployed an application through a Jenkins pipeline.
- Verified application deployment through a web browser.

## Project Status

Successfully tested GitHub checkout, Docker image building, and container deployment through Jenkins.
