# 🚀 Deploy an App with Docker & AWS

This project demonstrates how I successfully deployed a **web application** using **Docker** and **AWS Elastic Beanstalk**.  

---

## 📖 Project Overview

- Learned the fundamentals of **containers** and **Docker**.  
- Built and deployed a **custom Docker image** for my own web app.  
- Ran and tested it locally using **Nginx**.  
- Finally deployed the app on **AWS Elastic Beanstalk**.  

---

## 🐳 What is Docker?

Docker is a containerization platform that allows developers to package applications with everything they need (code, libraries, dependencies) into a **container** that runs anywhere.  

Key Components:
- **Dockerfile** → Instructions for building custom images.  
- **Docker Image** → Blueprint of the application environment.  
- **Docker Container** → Running instance of the image.  
- **Docker Daemon** → Manages containers in the background.  

---

## ⚙️ Steps in the Project

### 1️⃣ Running an Nginx Container
```bash
docker run -d -p 80:80 nginx
```
This command runs an Nginx web server in a container, serving files on port 80.

---

### 2️⃣ Creating a Custom Image
I wrote a `Dockerfile` that:  
1. Started from the latest **Nginx image**.  
2. Replaced the default HTML file with my own.  
3. Exposed **port 80** for web traffic.  

Build command:
```bash
docker build -t my-web-app .
```

---

### 3️⃣ Running My Custom Image
If another container is already using port 80, stop it first:
```bash
docker stop <CONTAINER_ID>
```
Then run the custom image.

---

### 4️⃣ Deploying with AWS Elastic Beanstalk
Elastic Beanstalk makes deploying Docker containers on AWS easier.  
Steps:  
- Built and tested locally.  
- Pushed custom Docker image.  
- Deployed using **Elastic Beanstalk**.  

⏱️ This step took me **a couple of hours**, mainly due to **IAM permission issues**.

---

## 📸 Screenshots / Demo

Here are some screenshots of the project in action:  

### 🔹 Running Locally
![Local Nginx Container](https://drive.google.com/file/d/1VStLV1i9vEbilr4PtDndjQ9oJD6eSgl3/view)  

### 🔹 Custom Docker Image
![Custom Image](screenshots/custom-image.png)  

### 🔹 AWS Elastic Beanstalk Deployment
![AWS Deployment](screenshots/aws-deploy.png)  

### 🔹 Live Demo (Optional)
👉 [Live App URL](#)  

*(Replace `screenshots/*.png` with your actual screenshot file paths and update the demo link if available)*  

---

## ⏳ Time Taken
The project took around **2–3 hours** in total.  
- Most challenging part → Setting up **IAM user permissions** in AWS.  
- Most rewarding part → Successfully deploying my own web app with Docker & AWS.  

---

## 🌐 Resources
- [Docker Documentation](https://docs.docker.com/)  
- [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)  

---

## 👨‍💻 Author
**Rajesh Biswas**  
NextWork Student – [nextwork.org](https://nextwork.org)

---
