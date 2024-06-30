# Docker & Basic App Deploy on Docker Hub 🚀

### What is Docker? 🐳

Docker is a platform for developing, shipping, and running applications using containerization technology. It provides tools and a runtime environment for creating, managing, and deploying containers. Docker simplifies the process of building, distributing, and running applications by packaging them into standardized containers.

### What is an Image? 📦

An image in the context of containerization refers to a lightweight, standalone, executable software package that contains all the necessary dependencies to run a piece of software. It is a snapshot of a container that includes the application code, runtime, system tools, libraries, and configuration files needed to run the software.

### What is a Container? 🛠️

A container is a runtime instance of an image that encapsulates an application and its dependencies, running in an isolated environment. It provides a lightweight, portable, and consistent execution environment for applications across different computing environments. Containers share the host operating system kernel but are isolated from each other, providing process and resource isolation.

### What is Docker Hub? 🌐

Docker Hub is a cloud-based repository for storing and sharing Docker images. It provides a centralized location for developers to publish and discover containerized applications and services. Docker Hub hosts millions of public images, including official images maintained by Docker, as well as user-contributed images.

## Getting Started 🏁

### Prerequisites 📋

- [Docker](https://www.docker.com/products/docker-desktop) installed on your machine.
- [Node.js](https://nodejs.org/) installed on your machine.

### Project Structure 🗂️

1. Create react based web app

follow this command if react is not installed
```bash
npm install -g create-react-app
```
```bash
npx create-react-app testapp
```
2. Create Docker File provided in repository can download Node form docker hub.

3. Build Docker Image
```bash
docker build .
```
Build Image with tag
```bash
docker build -t mywebapp01 .
```

4. list the Docker Images
```bash
docker image ls
```

5. list Running containers
```bash
dcoker ps
```
list all containers
```bash
dcoker ps -a
```

6. Start a Docker container from an image and map ports between the host and the container.
```bash
docker run –p 3000:3000 image_id
docker run -d --rm --name "mywebaap" –p 3000:3000 image_id
```
-d: This option runs the container in detached mode, meaning it runs in the background.

--rm: This option automatically removes the container when it exits, which helps in cleaning up after temporary containers.

--name "my_webapp": This option assigns a name to the container. In this case, the container is named "my_webapp". Naming a container makes it easier to reference it later (e.g., for stopping or inspecting the container).

7. Update the project
   
i. Create new version to update a project by using new build

```bash
docker build –t mywebapp:02
```

ii. After that run the docker container on different port
```bash
docker run -d --name "mywebapp" -p 3001:3000 image_id
```
### Some Key Points:

* You can run multiple versions of the application simultaneously using different tags and ports. This allows for easy comparison and rollback if necessary.
* Make sure to specify different host ports for each version to avoid conflicts.


8. Delete Image

```bash
docker rmi mywebapp:02
```

9. Stop running container
```bash
docker stop ‘container name’
```

### Screenshots

![Screenshot (39)](https://github.com/Aman8593/Docker/assets/104978692/620f820b-61ac-4bb7-826b-c04f7b5bceaf)

![Screenshot (40)](https://github.com/Aman8593/Docker/assets/104978692/3b2e1530-0828-431b-b7d8-fafbd622e3fc)

![Screenshot (41)](https://github.com/Aman8593/Docker/assets/104978692/76022da2-14ad-4020-b3ef-81b2d7d5e03a)

![Screenshot (42)](https://github.com/Aman8593/Docker/assets/104978692/7838aeb1-2bc6-497e-87e4-2f757f83d8bc)

![Screenshot (43)](https://github.com/Aman8593/Docker/assets/104978692/fd2c3e66-f6de-4f4d-8f11-a0b873094718)

![Screenshot (44)](https://github.com/Aman8593/Docker/assets/104978692/4db54685-54c7-4cf0-b89b-6e67d414ceda)

![](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.altexsoft.com%2Fblog%2Fdocker-pros-and-cons%2F&psig=AOvVaw1o4ElQyKbeAeqiyKiB6iHG&ust=1719845198958000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCIjWw-fIg4cDFQAAAAAdAAAAABAR)

