# DockerTest - Spring Boot Dockerized App 🚀🐳

This project demonstrates how to containerize a Spring Boot application using Docker and share it via Docker Hub.

---

## 🧾 Project Structure

DockerTest/
├── target/
│ └── DockerTest-3.5.3.jar
├── Dockerfile
├── pom.xml


---

## ⚙️ Prerequisites

- Java (e.g., JDK 21)
- Maven
- Docker Desktop (installed and running)
- Docker Hub account (e.g., `carrot`)

---

## 🛠️ Steps to Build & Run

1. 🧪 Build the Spring Boot App with Maven

```bash
mvn clean install

2. 📦 Create a Dockerfile(file name is a key, and should be "Dockerfile")

FROM eclipse-temurin:21-jdk-alpine
WORKDIR /app
COPY target/DockerTest-3.5.3.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]

3. 🏗️ Build the Docker Image
docker build -t docker-test-app .

4. 🧪 Run the Docker Container (Locally)
docker run -p 8080:8080 docker-test-app

☁️ Push to Docker Hub
5. 🔑 Log in to Docker Hub
docker login

6. 🏷️ Tag the Docker Image
docker tag docker-test-app carrot/docker-test-app:latest
carrot here is user_name.

7. 🚀 Push to Docker Hub
docker push carrot/docker-test-app:latest


The image will be available at:
👉 https://hub.docker.com/r/carrot/docker-test-app





