# Jenkins CI/CD Pipeline

## DevOps Internship - Task 2

This project demonstrates a simple CI/CD pipeline using Jenkins and Docker.

## Technologies Used

- Jenkins
- GitHub
- Node.js
- Docker
- npm

## Project Workflow

The Jenkins pipeline performs the following stages:

1. Checkout - Retrieves the source code from GitHub.
2. Build - Installs Node.js dependencies using npm.
3. Test - Runs the application tests.
4. Deploy - Builds a Docker image and runs the application in a Docker container.

## CI/CD Pipeline

GitHub
↓
Jenkins
↓
Checkout
↓
Build
↓
Test
↓
Docker Build
↓
Docker Container
↓
Node.js Application

## Application

The Node.js application runs on port 3000.

URL:

http://localhost:3000

## Docker

Docker image:

nodejs-demo-app:latest

Docker container:

nodejs-demo-container

## Result

The Jenkins pipeline successfully builds, tests, and deploys the Node.js application using Docker.