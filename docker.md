Here’s an explanation of each command along with a properly formatted presentation:

---

### **Commands to Run MySQL and Student App in Docker**

#### 1. **Run a MySQL Container**
```bash
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test_db -p 3306:3306 -d mysql:latest
```
- **`--name mysql-container`**: Names the container as `mysql-container`.
- **`-e MYSQL_ROOT_PASSWORD=password`**: Sets the root password for the MySQL database to `password`.
- **`-e MYSQL_DATABASE=test_db`**: Creates a database named `test_db` during initialization.
- **`-p 3306:3306`**: Maps port `3306` of the host to port `3306` of the container.
- **`-d`**: Runs the container in detached mode.
- **`mysql:latest`**: Specifies the latest version of the MySQL image.

#### 2. **Run the Student App Container**
```bash
docker run -it --name student-app --link mysql-container:mysql-container -p 8081:8080 -e SPRING_DATASOURCE_URL=jdbc:mysql://mysql-container:3306/test_db -e SPRING_DATASOURCE_USERNAME=root -e SPRING_DATASOURCE_PASSWORD=password -d student-app
```
- **`-it`**: Allows interaction with the container if needed.
- **`--name student-app`**: Names the container as `student-app`.
- **`--link mysql-container:mysql-container`**: Links the `student-app` container to the `mysql-container`.
- **`-p 8081:8080`**: Maps port `8080` of the container to port `8081` on the host.
- **`-e SPRING_DATASOURCE_URL=jdbc:mysql://mysql-container:3306/test_db`**: Sets the datasource URL to point to the MySQL database in the linked container.
- **`-e SPRING_DATASOURCE_USERNAME=root`**: Sets the username for the database connection as `root`.
- **`-e SPRING_DATASOURCE_PASSWORD=password`**: Sets the password for the database connection as `password`.
- **`-d student-app`**: Runs the `student-app` image in detached mode.

---

### **Command to Connect Student App to Host MySQL**
```bash
docker run -it --name student-app-container --network host -d student-app
```
- **`--network host`**: Makes the container use the host's networking stack, allowing direct communication with MySQL running on the host.
- **`--name student-app-container`**: Names the container as `student-app-container`.
- **`-d student-app`**: Runs the `student-app` image in detached mode.

---

### **Run Queries in the MySQL Container**
1. Connect to the MySQL container:
```bash
winpty docker exec -it <mysql-container-id> mysql -u root -p
```
- **`winpty`**: Ensures proper terminal handling in environments like Windows.
- **`docker exec -it <mysql-container-id>`**: Opens an interactive terminal session to the running container with the specified ID.
- **`mysql -u root -p`**: Launches the MySQL CLI with the username `root`. The password will be prompted.

2. Example using a specific container ID:
```bash
winpty docker exec -it c3bd578de7bb3a2a01be54eaf7a19a07f5cb929276da613dde6693223d3e6df0 mysql -u root -p
```

---

### **Docker Login**
```bash
docker login
```
- Prompts for Docker Hub credentials to authenticate and allow pushing/pulling images from your Docker Hub account.

---

### **Tagging the Docker Image**
```bash
docker tag student-app siddarthinme/student-app:latest
```
- **`docker tag student-app`**: Refers to the local `student-app` image.
- **`siddarthinme/student-app:latest`**: Tags the image to your Docker Hub repository under the name `siddarthinme` and `student-app` with the `latest` tag.

---

### **Push the Image to Docker Hub**
```bash
docker push siddarthinme/student-app:latest
```
- **`docker push siddarthinme/student-app:latest`**: Pushes the `latest` tag of `student-app` to the repository `siddarthinme` on Docker Hub.

---

These commands detail how to set up a MySQL container, run a Spring Boot application (`student-app`), manage Docker networking, interact with MySQL inside a container, and push the application image to Docker Hub.
