<<<<<<< HEAD
Containerization & Deployment

I created separate Dockerfiles for the backend and frontend, built the images locally, and pushed them to Docker Hub. On AWS, I launched an Ubuntu server, installed Docker and Docker Compose, and created a docker-compose.yml file defining three services: MongoDB as the database container, the backend pulling its image from Docker Hub and connecting to MongoDB, and the frontend pulling its image from Docker Hub and connecting to the backend. When deployed, the MongoDB container starts first, followed by the backend and frontend, and all services run successfully, making the full MEAN stack application live.


Result:

MongoDB container starts first.

Backend pulls the image from Docker Hub and connects to MongoDB.

Frontend pulls the image from Docker Hub and connects to the backend.

All services run successfully, making the full MEAN stack application live.
