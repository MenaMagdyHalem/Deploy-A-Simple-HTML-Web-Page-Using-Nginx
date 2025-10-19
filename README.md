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

---


