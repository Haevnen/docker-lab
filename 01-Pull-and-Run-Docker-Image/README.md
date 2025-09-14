# How to Pull and Run Docker Images from Docker Hub and Run

## Step 1: Pull Docker Image from Docker Hub

```bash
# List Docker images
docker images

# Pull Docker image from Docker Hub
docker pull stacksimplify/mynginx:v1
```

## Step 2: Run the downloaded Docker Image

```bash
# Run Docker container
docker run --name <CONTAINER_NAME> -p <HOST_PORT>:<CONTAINER_PORT> -d <IMAGE_NAME>:<TAG>

# Example
docker run --name mynginx -p 8080:80 -d stacksimplify/mynginx:v1
```

## Step 3: Access the application
- Open browser and navigate to [http://localhost:8080/](http://localhost:8080/)

## Step 4: List running containers

```bash
# Only running containers
docker ps

# All containers (including stopped ones)
docker ps -a

# Only container IDs
docker ps -q
```

## Step 5: Access container terminal

```bash
# Connect to the container's terminal
docker exec -it <CONTAINER_NAME> /bin/sh

# Example
docker exec -it mynginx /bin/sh

# Exec command directly
docker exec -it mynginx ls
```

## Step 6: Stop/start and remove containers

```bash
# Stop a running container
docker stop <CONTAINER_NAME>

# Start the stopped container
docker start <CONTAINER_NAME>

# Remove the container
docker rm <CONTAINER_NAME>

# or stop and remove in one command
docker rm -f <CONTAINER_NAME>
```

## Step 7: Remove Docker image
```bash
# List Docker images
docker images

# Remove image by ID
docker rmi <IMAGE_ID>
```