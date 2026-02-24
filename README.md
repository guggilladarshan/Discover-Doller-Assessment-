<<<<<<< HEAD
Containerization & Deployment

The application has been fully containerized and deployed on a cloud Ubuntu server. Here's the workflow:

Dockerization:

Created separate Dockerfiles for the backend and frontend.

Built images locally and pushed them to Docker Hub:

Cloud VM Setup:

Launched an Ubuntu server on a cloud platform (AWS, Azure, or GCP).

Installed Docker and Docker Compose on the server.

Docker Compose Deployment:

Created a docker-compose.yml on the server.

The compose file includes three services:

MongoDB – database container.

Backend – pulls the backend image from Docker Hub.

Frontend – pulls the frontend image from Docker Hub.


Result:

MongoDB container starts first.

Backend pulls the image from Docker Hub and connects to MongoDB.

Frontend pulls the image from Docker Hub and connects to the backend.

All services run successfully, making the full MEAN stack application live.
