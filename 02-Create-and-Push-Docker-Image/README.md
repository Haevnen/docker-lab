## 1. What is Dockerfile
- Dockerfile is a simple text file that contains set of instructions to build a
  Docker image.

## 2. Build a Docker image
```bash
# Build an image
docker build -t <IMAGE_NAME>:<TAG> .

# Example:
docker build -t nginx-custom:v1 .

# List and Run a new Docker image
docker images

docker run --name <CONTAINER_NAME> -p <HOST_PORT>:<CONTAINER_PORT> -d <IMAGE_NAME>:<TAG>

# Example:
docker run --name mynginx1 -p 8090:80 -d nginx-custom:v1

# Access the application in your browser
http://localhost:8090
```

## 3. Tag and Push the image to Docker Hub
```bash

# Tag the Docker image
docker tag nginx-custom:v1 <YOUR_DOCKER_USERNAME>/nginx-custom:v1

# Example
docker tag nginx-custom:v1 haevnen/nginx-custom:v1

# Push the image to Docker Hub
docker push haevnen/nginx-custom:v1
```