# 🚀 Deploy a Simple Website Using Nginx & Docker

This project demonstrates how to **deploy a static website using Nginx inside a Docker container**.  
It covers the full workflow — from cloning a website, building a Docker image, running a container, and finally pushing the image to **Docker Hub**.

---

## 📋 Table of Contents

1. [Overview](#-project-overview)
2. [Technologies Used](#-technologies-used)
3. [Project Structure](#-project-structure)
4. [Dockerfile](#-dockerfile)
5. [Steps to Deploy](#-steps-to-deploy)
6. [Accessing the Website](#-accessing-the-website)
7. [Commit & Push to Docker Hub](#-commit--push-to-docker-hub)
8. [Summary](#-summary)
9. [Author](#-author)
10. [License](#-license)

---

## 🧩 Project Overview

In this project, we will:

1. Clone an existing website from GitHub  
2. Create a Dockerfile for Nginx  
3. Build a Docker image  
4. Run a Docker container  
5. Access the website locally  
6. Commit the container and push it to Docker Hub  

This is a **beginner-friendly DevOps project** showing how Docker simplifies web deployment.

---

## 🛠️ Technologies Used

| Tool / Technology | Purpose |
|--------------------|----------|
| **Nginx** | Web server to serve static website |
| **Docker** | Containerization platform |
| **GitHub** | Version control & code hosting |
| **Docker Hub** | Image registry to store built images |
| **Linux (Ubuntu)** | Host operating system |

---
## 🐳 Dockerfile

The Dockerfile defines the environment and deployment steps.

```dockerfile
# Use the official Nginx image as the base
FROM nginx:latest

# Copy website files into the Nginx web directory
COPY ./Course-Docker/sample-website /usr/share/nginx/html/

# Expose port 80 for HTTP traffic
EXPOSE 80
```
---

## ⚙️ Steps to Deploy

Follow these steps carefully to reproduce the project.


## 🔹 Step 1: Clone the Website Repository

First, clone the website source from GitHub:

```bash
git clone https://github.com/MenaMagdyHalem/Course-Docker.git
```

##🔹 Step 2: Go Inside the Website Folder
```bash
cd sample-website/
ls
```

## 🔹 Step 3: Create a Dockerfile
```bash
cd ~
vim Dockerfile
```

## 🔹 Step 4: Build the Docker Image
Now build the Docker image and tag it as website:
```bash
docker build -t website .

```

## 🔹 Step 5: Run the Container
```bash
docker run -it --rm -d -p 3000:80 --name web website
```

## 🔹 Step 6: Verify the Container is Running
```bash
docker ps
CONTAINER ID   IMAGE     COMMAND                  PORTS                  NAMES
df46ef6b0769   website   "/docker-entrypoint.…"   0.0.0.0:3000->80/tcp   web
```

## 🔹 Step 7: Access the Website

Now open your browser and visit:

👉 http://localhost:3000
or
👉 http://<your-server-IP>:3000
You should see your static website running successfully via Nginx inside Docker 🎉

## 🔹 Step 8: Commit the Running Container
Once you confirm the container works, save it as a new image:
```bash
docker commit web menamagdyhalem/new-web
```
List your images again:
```bash
docker images
```

## Step 9: Login to Docker Hub
Login using your Docker Hub credentials:
```bash
docker login
```
Enter your username and password when prompted.

## 🔹 Step 10: Push Image to Docker Hub
Push your new image to your Docker Hub repository:
```bash
docker push <user-name-account>/new-web
```

## 👨‍💻 Author
Mena Magdy Halem
Instructor & DevOps Engineer







