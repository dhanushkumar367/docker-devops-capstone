
# Docker DevOps Capstone

## Project Title
Containerize and Deploy a Version-Controlled Web Application Using Docker

## Objective
Create a website, manage its source code using Git and GitHub,
package it into Docker images and run two versions in separate
containers using different host ports.

## Technologies
- HTML and CSS
- Git and GitHub
- Docker Desktop
- Dockerfile
- NGINX Alpine

## Architecture
Website Source -> GitHub -> Dockerfile -> Docker Images
-> Docker Containers -> Browser

## Docker Images
- devops-showcase:v1
- devops-showcase:v2

## Containers and Ports
- showcase-v1: localhost:8080 -> container port 80
- showcase-v2: localhost:8081 -> container port 80

## Build Commands
docker build -t devops-showcase:v1 .
docker build -t devops-showcase:v2 .

## Run Commands
docker run -d --name showcase-v1 -p 8080:80 devops-showcase:v1
docker run -d --name showcase-v2 -p 8081:80 devops-showcase:v2

## Verification
docker images
docker ps
docker history devops-showcase:v1
docker history devops-showcase:v2

## Expected Outcome
Two independent website versions running in separate
Docker containers, with the source code hosted on GitHub.
