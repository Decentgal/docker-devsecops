
Dockerized High-Performance Web Infrastructure

This repository contains a containerized multi-page web application optimized for production environments. It serves as a blueprint for Infrastructure-as-Code (IaC), using Docker and NGINX to provide a consistent, scalable, and portable environment for frontend delivery.

The project demonstrates a transition from traditional hosting to modern DevSecOps practices, focusing on minimal image footprints and automated deployment readiness.


Architectural Features

Production-Grade Web Server: Leverages an NGINX base image for high-concurrency static content delivery.

Modular Asset Pipeline: Separates styling (SCSS), logic (JS), and assets (fonts/images) for clean build contexts.

Environment Parity: Eliminates "works on my machine" issues by encapsulating the entire runtime environment.

Scalable Design: Ready for orchestration via Kubernetes or Docker Compose.


Technology Stack

Containerization: Docker

Web Server: NGINX

Frontend Architecture: HTML5, SCSS (Sass), JavaScript

Version Control: Git


Steps

1. Build the Infrastructure

Execute the following bash commands to build the optimized Docker image:
docker build -t devsecops-web-app:latest .

2. Deploy the Container

Launch the application on port 8080:
docker run -d -p 8080:80 --name web-infrastructure devsecops-web-app:latest

3. Access the application on a browser at: http://localhost:8080


Repository Structure

.github/workflows/ = CI/CD pipeline definitions

css/               = Compiled SCSS stylesheets

fonts/             = Custom typography assets

images/            = Optimized UI assets

js/                = Client-side logic

Dockerfile         = Infrastructure-as-Code definition

index.html         = Landing page

[about/menu/book]  = Application modules
