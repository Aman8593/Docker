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
2.Create Docker File provided in repository

3.To build Docker Image
```bash
docker build .
```
Build Image with tag
```bash
docker build -t mywebapp01 .
```

