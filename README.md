Task-2_Internshipp


# 📦 Spring Boot Application

This is a simple yet complete Spring Boot web application demonstrating a full DevOps lifecycle. It includes:

- Java + Spring Boot backend
- Static frontend resources (HTML/CSS)
- In jenkins uses Docker as Agent
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


![4](https://github.com/user-attachments/assets/9c911bef-66bd-4a39-95ca-0e12ef927b45)




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

![1](https://github.com/user-attachments/assets/50e4c61a-2892-4eea-9ac5-3dc90fbade11)




![2](https://github.com/user-attachments/assets/e7422ab1-ecb6-47e3-8b94-8ce8f994449d)




------------------------------------------------------------------------------------------- 


## 🔍 SonarQube Integration

SonarQube is integrated into the Jenkins pipeline for code quality analysis.

### SonarQube

![3](https://github.com/user-attachments/assets/2ed96d2f-6f72-4a37-8f32-7c9da95f5923)



It highlights potential bugs, code smells, and vulnerabilities. It ensures the application meets quality standards before proceeding to build and deployment.

---

## 🚀 Application Running

Finally, here's the application up and running:


![5](https://github.com/user-attachments/assets/40c4ac37-dee6-4f06-8f24-af159ad15c26)


