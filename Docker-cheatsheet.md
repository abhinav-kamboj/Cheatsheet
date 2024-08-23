# Docker Cheat Sheet

Docker is an open-source platform that enables developers to build, deploy, and manage applications within lightweight, portable containers. It allows us to package an application with all its dependencies into a standardized unit for software development.

## Basic Commands

- **Check Docker Version**:  
  ```bash
  docker version
  ```

- **Get System Info**:  
  ```bash
  docker system info
  ```

- **Help Command**:  
  ```bash
  docker help
  ```  
  or  
  ```bash
  docker <command> --help
  ```

## Container Management

- **Run a Container**:  
  ```bash
  docker run [options] IMAGE
  ```
  (e.g., `docker run -d -p 8080:80 nginx`)

- **List Running Containers**:  
  ```bash
  docker ps
  ```

- **List All Containers**:  
  ```bash
  docker ps -a
  ```

- **Stop a Container**:  
  ```bash
  docker stop <container-id>
  ```
  (e.g., `docker stop 1b1a3lcf`)
- **Remove a Container**:  
  ```bash
  docker rm <container-id>
  ```
  (e.g., `docker rm 1b1a3lcf`)
## Image Management

- **Build an Image**:  
  ```bash
  docker build -t <image_name> .
  ```
  (e.g., `docker build -t myapp .`)
- **List Images**:  
  ```bash
  docker images
  ```

- **Pull an Image**:  
  ```bash
  docker pull <image_name>
  ```
  (e.g., `docker pull ubuntu`)

- **Push an Image**:  
  ```bash
  docker push <username>/<image_name>
  ```
  (e.g., `docker push myusername/myapp`)
- **Remove an Image**:  
  ```bash
  docker rmi <image_id>
  ```
  (e.g., `docker rmi myapp`)
- **Tag an Image**:  
  ```bash
  docker tag <source_image> <target_image>:<tag>
  ```  
  (e.g., `docker tag myapp:latest myapp:v1.0`)

## Networking

- **Create a Network**:  
  ```bash
  docker network create <network_name>
  ```

- **List Networks**:  
  ```bash
  docker network ls
  ```

- **Connect a Container to a Network**:  
  ```bash
  docker network connect <network_name> <container_id>
  ```

## Volume Management

- **Create a Volume**:  
  ```bash
  docker volume create <volume_name>
  ```

- **List Volumes**:  
  ```bash
  docker volume ls
  ```

- **Remove a Volume**:  
  ```bash
  docker volume rm <volume_name>
  ```

## Docker Compose

- **Start Services**:  
  ```bash
  docker-compose up
  ```

- **Stop Services**:  
  ```bash
  docker-compose down
  ```

## Dockerfile Instructions

- **FROM**: Sets the base image.
- **RUN**: Executes commands in a new layer.
- **COPY**: Copies files/directories into the image.
- **CMD**: Provides defaults for an executing container.
- **ENTRYPOINT**: Configures a container to run as an executable.
- **EXPOSE**: Informs Docker that the container listens on specified ports.

### Example Dockerfile

```dockerfile
# Use the official Node.js image as the base image
FROM node:14

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm ci

# Copy the application code to the working directory
COPY . .

# Build the application
RUN npm run build

# Expose port 3000 for the application
EXPOSE 3000

# Set the command to start the application
CMD ["npm", "start"]
```

## Security

- **Scan for Vulnerabilities**:  
  ```bash
  docker scout cves <image_name>
  ```
  (e.g., `docker scout cves myapp`)
