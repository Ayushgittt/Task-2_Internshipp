# Task-2_Internshipp

# 📦 Spring Boot Application

This is a simple yet complete Spring Boot web application demonstrating a full DevOps lifecycle. It includes:

- Java + Spring Boot backend
- Static frontend resources (HTML/CSS/JS)
- Docker support
- CI/CD pipeline using Jenkins on AWS
- Code quality checks using SonarQube

---

## 🐳 Dockerfile

The project includes a `Dockerfile` for building the application image. It uses a multi-stage build process:

```Dockerfile
FROM maven:3.8.1-openjdk-17 AS build
COPY . /app
WORKDIR /app
RUN mvn clean package -DskipTests

FROM openjdk:17
COPY --from=build /app/target/*.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]
```

This Dockerfile ensures the final image is lean and production-ready, containing only the compiled JAR.

---

## ☁️ Jenkins on AWS

Jenkins is hosted on an AWS EC2 instance to automate the CI/CD process. Below are some screenshots of the Jenkins setup and job execution:

### Jenkins Dashboard

![Jenkins Dashboard](1.png)

### Jenkins Job Configuration

![Jenkins Job](2.png)

---

## 📜 Jenkinsfile

The pipeline is defined in a `JenkinsFile` with the following stages:

- **Clone Repository**
- **Build with Maven**
- **Run SonarQube Analysis**
- **Build Docker Image**
- **Push to DockerHub**
- **Deploy to EC2**

Example snippet:

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('MySonarServer') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
```

### Jenkins Build Output

![Jenkins Build Output](3.png)

---

## 🔍 SonarQube Integration

SonarQube is integrated into the Jenkins pipeline for code quality analysis.

### SonarQube Report

![SonarQube](4.png)

The report highlights potential bugs, code smells, and vulnerabilities. It ensures the application meets quality standards before proceeding to build and deployment.

---

## 🚀 Application Running

Finally, here's the application up and running:

![Application Screenshot](5.png)

The app is accessible via a public IP on your EC2 server, showcasing a complete CI/CD workflow from code to production.
