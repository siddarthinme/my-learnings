Here’s a list of basic Docker commands, categorized for better understanding, along with a brief explanation of each:

---

### **1. Docker Installation and Version**
- **`docker --version`**
  - Displays the installed Docker version.
- **`docker info`**
  - Shows system-wide Docker information, such as the number of containers, images, and resources.

---

### **2. Container Management**
- **`docker ps`**
  - Lists currently running containers.
- **`docker ps -a`**
  - Lists all containers, including stopped ones.
- **`docker run`**
  - Creates and starts a new container.
  - Example: `docker run -it ubuntu` starts an interactive Ubuntu container.
- **`docker start <container-id>`**
  - Starts an existing stopped container.
- **`docker stop <container-id>`**
  - Stops a running container.
- **`docker restart <container-id>`**
  - Restarts a container.
- **`docker rm <container-id>`**
  - Removes a stopped container.
- **`docker kill <container-id>`**
  - Forcefully stops a container.
- **`docker exec`**
  - Runs a command in an already running container.
  - Example: `docker exec -it <container-id> bash` opens an interactive shell inside a container.

---

### **3. Image Management**
- **`docker images`**
  - Lists all locally available Docker images.
- **`docker pull <image>`**
  - Downloads a Docker image from Docker Hub or another registry.
- **`docker build`**
  - Builds a Docker image from a `Dockerfile`.
  - Example: `docker build -t my-app .` builds an image named `my-app`.
- **`docker rmi <image-id>`**
  - Removes an image by ID.
- **`docker tag <image> <repository>:<tag>`**
  - Tags an image for a repository.
  - Example: `docker tag my-app myrepo/my-app:latest`.
- **`docker push <repository>:<tag>`**
  - Pushes a tagged image to a Docker registry.

---

### **4. Networking**
- **`docker network ls`**
  - Lists all Docker networks.
- **`docker network create <network-name>`**
  - Creates a new Docker network.
- **`docker network inspect <network-name>`**
  - Displays detailed information about a Docker network.
- **`docker network connect <network-name> <container-id>`**
  - Connects a container to a network.
- **`docker network disconnect <network-name> <container-id>`**
  - Disconnects a container from a network.

---

### **5. Volumes and Storage**
- **`docker volume ls`**
  - Lists all Docker volumes.
- **`docker volume create <volume-name>`**
  - Creates a new volume.
- **`docker volume inspect <volume-name>`**
  - Displays detailed information about a volume.
- **`docker volume rm <volume-name>`**
  - Removes a volume.
- **`docker run -v <volume-name>:<path>`**
  - Mounts a volume to a container.
  - Example: `docker run -v my-volume:/data my-app`.

---

### **6. Logs and Monitoring**
- **`docker logs <container-id>`**
  - Displays logs of a container.
- **`docker logs -f <container-id>`**
  - Follows (streams) the logs of a container.
- **`docker stats`**
  - Shows real-time resource usage of containers.
- **`docker inspect <container-id>`**
  - Displays detailed information about a container.

---

### **7. Docker Compose**
- **`docker-compose up`**
  - Starts all services defined in a `docker-compose.yml` file.
- **`docker-compose down`**
  - Stops and removes containers, networks, and volumes created by `docker-compose up`.
- **`docker-compose logs`**
  - Displays logs for all services in the `docker-compose.yml`.

---

### **8. Advanced Commands**
- **`docker save <image> -o <file>`**
  - Saves a Docker image to a tar archive.
  - Example: `docker save my-app -o my-app.tar`.
- **`docker load -i <file>`**
  - Loads a Docker image from a tar archive.
  - Example: `docker load -i my-app.tar`.
- **`docker export <container-id> -o <file>`**
  - Exports a container’s filesystem to a tar file.
- **`docker import <file>`**
  - Creates a Docker image from a tar file.

---

### **9. Cleanup**
- **`docker system prune`**
  - Removes unused Docker data like stopped containers, dangling images, and unused networks.
- **`docker image prune`**
  - Removes unused images.
- **`docker container prune`**
  - Removes stopped containers.
- **`docker volume prune`**
  - Removes unused volumes.

---

These commands provide the foundational skills for working with Docker. For practical use, understanding container and image management, networking, and volumes is crucial.
