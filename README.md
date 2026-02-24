<<<<<<< HEAD
Containerization & Deployment

I created separate Dockerfiles for the backend and frontend, built the images locally, and pushed them to Docker Hub. On AWS, I launched an Ubuntu server, installed Docker and Docker Compose, and created a docker-compose.yml file defining three services: MongoDB as the database container, the backend pulling its image from Docker Hub and connecting to MongoDB, and the frontend pulling its image from Docker Hub and connecting to the backend. When deployed, the MongoDB container starts first, followed by the backend and frontend, and all services run successfully, making the full MEAN stack application live.


Result:

MongoDB container starts first.

Backend pulls the image from Docker Hub and connects to MongoDB.

Frontend pulls the image from Docker Hub and connects to the backend.

All services run successfully, making the full MEAN stack application live.



<<<<<<<<<<<  HEAD
Jenkins CI/CD Pipeline for MEAN Stack Application

CI/CD pipeline using Jenkins to automate the build, Dockerization, and deployment of a MEAN stack (MongoDB, Express, Angular, Node.js) CRUD application.


The Jenkins pipeline automates the following steps:

Pull latest code from GitHub

Build Docker images for backend and frontend

Push Docker images to Docker Hub

Deploy updated application on the cloud server using Docker Compose

Jenkins Pipeline Steps
1. Pull Code from GitHub

Jenkins fetches the latest code from the repository whenever a commit is pushed to the main branch.

2. Build Docker Images

Builds separate Docker images for the backend and frontend using their respective Dockerfiles.

3. Push Images to Docker Hub

Logs into Docker Hub and pushes the newly built images.




