# Node.js & Docker Deployment App

## Project Overview

This project demonstrates the development and deployment of a simple Node.js application using GitHub, Linux, Docker, and Docker Hub.

The application was successfully containerized using Docker, pushed to Docker Hub, pulled from Docker Hub, and run as a Docker container.

## Technologies Used

* Node.js
* Git
* GitHub
* Linux / Ubuntu (WSL)
* Docker
* Docker Hub

## Application

The application is a simple Node.js web application that displays a successful deployment message and version information.

**Application:** Node.js & Docker Deployment App

**Version:** 1.0

**Port:** 3000

---

## 1. Node.js Application

The application source code contains the necessary files required to run and containerize the application.

Main project files include:

* app.js
* package.json
* package-lock.json
* Dockerfile
* .dockerignore
* .gitignore
* README.md

The project source code is hosted on GitHub.

**GitHub Repository:**
https://github.com/asogwajulie/nodejs-docker-app

---

## 2. Clone Application to Linux

The GitHub repository was cloned into an Ubuntu Linux environment using:

```bash
git clone https://github.com/asogwajulie/nodejs-docker-app.git
```

The project files were then verified in the Linux environment.

---

## 3. Dockerfile

A Dockerfile was created to define how the Node.js application would be packaged into a Docker image.

The Dockerfile uses the Node.js 22 base image, sets the application working directory, installs the application dependencies, copies the application files, and starts the Node.js application.

---

## 4. Build Docker Image

The Docker image was built and tagged using the Docker Hub username.

### Command

```bash
sudo docker build -t asogwajulie/nodejs-app:1.0 .
```

The Docker image was successfully built and tagged as:

```text
asogwajulie/nodejs-app:1.0
```

### Screenshot: Docker Build

![Docker Build](screenshots/docker-build.png)

The screenshot above shows the Docker build command and the successful completion of the Docker image build.

---
## 5. Push Image to Docker Hub

Docker was authenticated using:

```bash
sudo docker login
```

The Docker image was then pushed to Docker Hub using:

```bash
sudo docker push asogwajulie/nodejs-app:1.0
```

The image was successfully uploaded to the Docker Hub repository.

### Screenshot: Docker Hub Image

![Docker Hub Image](screenshots/docker-hub.png)

The screenshot above shows the Docker image available in the Docker Hub repository with the `1.0` tag.

---

## 6. Pull Image from Docker Hub

The Docker image was successfully pulled from Docker Hub using:

```bash
sudo docker pull asogwajulie/nodejs-app:1.0
```

The image was successfully available locally for running the application.

---

## 7. Run Docker Container

The Docker container was started using:

```bash
sudo docker run -d -p 3000:3000 --name nodejs-app asogwajulie/nodejs-app:1.0
```

The running container was verified using:

```bash
sudo docker ps
```

The container was successfully running and exposing port `3000`.

### Screenshot: Running Docker Container

![Running Docker Container](screenshots/docker-ps.png)

The screenshot above shows the Node.js Docker container running successfully.

---

## 8. Live Application

The deployed application was accessed through a web browser at:

```text
http://localhost:3000
```

The application displayed:

**Node.js & Docker Deployment App**

**Application successfully deployed and running.**

**Version 1.0**

### Screenshot: Live Application

![Live Application](screenshots/live-application.png)

The screenshot above confirms that the Node.js application is successfully running from the Docker container.

---

## Conclusion

The Node.js application was successfully developed, hosted on GitHub, cloned into a Linux environment, containerized using Docker, pushed to Docker Hub, pulled from Docker Hub, and run successfully as a Docker container.

The application was verified through a web browser and successfully displayed the deployment message on port `3000`.
