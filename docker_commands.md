# Docker Command Cheatsheet

## Basic Docker Commands

### **docker run**
- **Description**: Run a command in a new container.
- **Usage**: `docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]`
- **Example**: `docker run -it ubuntu bash`

### **docker ps**
- **Description**: List containers.
- **Usage**: `docker ps [OPTIONS]`
- **Example**: `docker ps -a` (lists all containers, even stopped ones)

### **docker images**
- **Description**: List images.
- **Usage**: `docker images [OPTIONS] [REPOSITORY[:TAG]]`
- **Example**: `docker images -a`

### **docker build**
- **Description**: Build an image from a Dockerfile.
- **Usage**: `docker build [OPTIONS] PATH | URL | -`
- **Example**: `docker build -t myapp .`

### **docker pull**
- **Description**: Pull an image or a repository from a registry.
- **Usage**: `docker pull [OPTIONS] NAME[:TAG|@DIGEST]`
- **Example**: `docker pull ubuntu:latest`

## Managing Containers

### **docker start**
- **Description**: Start one or more stopped containers.
- **Usage**: `docker start [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker start my_container`

### **docker stop**
- **Description**: Stop one or more running containers.
- **Usage**: `docker stop [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker stop my_container`

### **docker rm**
- **Description**: Remove one or more containers.
- **Usage**: `docker rm [OPTIONS] CONTAINER [CONTAINER...]`
- **Example**: `docker rm my_container`

### **docker exec**
- **Description**: Run a command in a running container.
- **Usage**: `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`
- **Example**: `docker exec -it my_container bash`

## Managing Images

### **docker rmi**
- **Description**: Remove one or more images.
- **Usage**: `docker rmi [OPTIONS] IMAGE [IMAGE...]`
- **Example**: `docker rmi ubuntu:latest`

### **docker tag**
- **Description**: Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.
- **Usage**: `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`
- **Example**: `docker tag ubuntu:latest myrepo/ubuntu:v1`

## Docker Networking

### **docker network**
- **Description**: Manage Docker networks.
- **Usage**: `docker network [COMMAND]`
- **Example**: 
  - `docker network ls` (list networks)
  - `docker network create mynet` (create a network)

## Docker Volumes

### **docker volume**
- **Description**: Manage Docker volumes.
- **Usage**: `docker volume [COMMAND]`
- **Example**: 
  - `docker volume create myvol`
  - `docker volume ls`
  
## Docker Compose (for managing multi-container Docker applications)

### **docker-compose up**
- **Description**: Build, (re)create, start, and attach to containers for a service.
- **Usage**: `docker-compose up [OPTIONS] [SERVICE...]`
- **Example**: `docker-compose up -d`

### **docker-compose down**
- **Description**: Stop and remove containers, networks, images, and volumes.
- **Usage**: `docker-compose down [OPTIONS]`
- **Example**: `docker-compose down`

---

This is just a basic overview. For more detailed information on each command, refer to the Docker documentation or use `docker [COMMAND] --help`.
