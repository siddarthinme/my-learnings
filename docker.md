Here's an explanation of each command and its purpose:

---

### **Build Docker Image**
```bash
docker build -t student-app .
```
- **docker build**: Builds a Docker image from the `Dockerfile` in the current directory (`.`).
- **-t student-app**: Tags the image with the name `student-app`.

---

### **Run MySQL Container**
```bash
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test_db -p 3306:3306 -d mysql:latest
```
- **docker run**: Runs a new container.
- **--name mysql-container**: Assigns the container the name `mysql-container`.
- **-e MYSQL_ROOT_PASSWORD=password**: Sets the root password for MySQL as `password`.
- **-e MYSQL_DATABASE=test_db**: Creates a database named `test_db`.
- **-p 3306:3306**: Maps port 3306 on the host to port 3306 on the container.
- **-d mysql:latest**: Runs the latest version of the official MySQL image in detached mode.

---

### **Run Student App Container**
```bash
docker run -it --name student-app --link mysql-container:mysql-container -p 8080:8080 -e SPRING_DATASOURCE_URL=jdbc:mysql://mysql-container:3306/test_db -e SPRING_DATASOURCE_USERNAME=root -e SPRING_DATASOURCE_PASSWORD=password -d student-app
```
- **docker run**: Runs a new container.
- **-it**: Interactive mode with a TTY (not mandatory in detached mode, but included here).
- **--name student-app**: Names the container `student-app`.
- **--link mysql-container:mysql-container**: Links the `mysql-container` to this container for inter-container communication.
- **-p 8080:8080**: Maps port 8080 on the host to port 8080 on the container.
- **-e SPRING_DATASOURCE_URL=jdbc:mysql://mysql-container:3306/test_db**: Sets the Spring Boot datasource URL environment variable to connect to the MySQL container.
- **-e SPRING_DATASOURCE_USERNAME=root**: Sets the database username as `root`.
- **-e SPRING_DATASOURCE_PASSWORD=password**: Sets the database password as `password`.
- **-d student-app**: Runs the `student-app` image in detached mode.

---

### **Run Queries in MySQL Container**
```bash
winpty docker exec -it <mysql-container-id> mysql -u root -p
```
- **winpty**: Allows running Docker commands interactively in Git Bash (required on Windows).
- **docker exec**: Executes a command in a running container.
- **-it**: Interactive mode with TTY.
- **<mysql-container-id>**: Replace with the actual container ID of `mysql-container`.
- **mysql -u root -p**: Opens the MySQL command-line client with the `root` user, prompting for the password.

Example:
```bash
winpty docker exec -it c3bd578de7bb3a2a01be54eaf7a19a07f5cb929276da613dde6693223d3e6df0 mysql -u root -p
```

---

### **Run Student App with Host Networking**
```bash
docker run -it --name student-app-container --network host -d student-app
```
- **docker run**: Runs a new container.
- **-it**: Interactive mode with TTY.
- **--name student-app-container**: Names the container `student-app-container`.
- **--network host**: Uses the host network directly, allowing the app to communicate with host services.
- **-d student-app**: Runs the `student-app` image in detached mode.

---

### **Docker Login**
```bash
docker login
```
- Logs into the Docker Hub registry, prompting for username and password.

---

### **Tag Docker Image**
```bash
docker tag student-app siddarthinme/student-app:latest
```
- **docker tag**: Tags an existing Docker image.
- **student-app**: The local image to be tagged.
- **siddarthinme/student-app:latest**: The repository name and tag on Docker Hub.

---

### **Push Docker Image to Docker Hub**
```bash
docker push siddarthinme/student-app:latest
```
- **docker push**: Pushes a Docker image to a remote registry.
- **siddarthinme/student-app:latest**: The tagged image to push.

---

### **Change Directory Permissions**
```bash
sudo chmod -R 777 student-app
```
- **sudo**: Executes the command with superuser privileges.
- **chmod**: Changes permissions of files/directories.
- **-R**: Applies changes recursively to all files and subdirectories.
- **777**: Grants read, write, and execute permissions to all users.
- **student-app**: The directory whose permissions are being changed.

---

### **Decode Base64 Strings**
```bash
echo "cm9vdA==" | base64 --decode
echo "<base64-encoded-username>" | base64 --decode
```
- **echo**: Outputs the string to the terminal.
- **base64 --decode**: Decodes a Base64-encoded string.
- Example:
  - **"cm9vdA=="** decodes to `root`.

--- 

These commands facilitate building, running, linking containers, pushing images to a registry, and performing administrative tasks like permission changes and string decoding.
