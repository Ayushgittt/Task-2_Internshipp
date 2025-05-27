<<<<<<< HEAD
Task-2_Internshipp


# 📦 Spring Boot Application

This is a simple yet complete Spring Boot web application demonstrating a full DevOps lifecycle. It includes:

- Java + Spring Boot backend
- Static frontend resources (HTML/CSS)
- Docker support
- CI/CD pipeline using Jenkins on AWS
- Code quality checks using SonarQube

---

## 🐳 Dockerfile

The project includes a `Dockerfile` for building the application image:

Build the Docker Image:

 docker build -t 8192027760/task-2:1 .
 
 docker run -d -p 8010:8080 -t 8192027760/task-2:1


Access the application on http:// <ip-address> :8010

This Dockerfile ensures the final image is production-ready, containing only the compiled JAR.


---

## ☁️ Jenkins on AWS

Jenkins is hosted on an AWS EC2 instance to automate the CI/CD process. Below are some screenshots of the Jenkins setup and job execution:


![4](https://github.com/user-attachments/assets/f87c0a69-66f7-40e6-8e5c-c9942966d138)


-------------------------------------------------------------------------------------------------------------------------------

## 📜 Jenkinsfile

The pipeline is defined in a `JenkinsFile` with the following stages:

- **Clone Repository**
- **Build with Maven**
- **Run SonarQube Analysis**
- **Build Docker Image**
- **Push to DockerHub**
- **Deploy to EC2**


-----------------------------------------------


### Jenkins Build Output

![1](https://github.com/user-attachments/assets/966f9411-ea3e-4c29-8517-d84bcefdd165)



![2](https://github.com/user-attachments/assets/ad2fbcc0-844f-435b-9ee8-dad946baadf2)



------------------------------------------------------------------------------------------- 


## 🔍 SonarQube Integration

SonarQube is integrated into the Jenkins pipeline for code quality analysis.

### SonarQube

![3](https://github.com/user-attachments/assets/943bd8e2-3599-4a77-bec5-6571b7e5c2bd)


It highlights potential bugs, code smells, and vulnerabilities. It ensures the application meets quality standards before proceeding to build and deployment.

---

## 🚀 Application Running

Finally, here's the application up and running:

![5](https://github.com/user-attachments/assets/61ba7186-3e51-4521-b887-6af5c1357cd7)
=======
# Task-2_Internshipp
>>>>>>> 251e438b7ed0471fa420951eb396313995a0baf0
