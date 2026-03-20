# my-app
# CI/CD Pipeline with Jenkins, SonarQube and Nexus

This project demonstrates a complete CI/CD pipeline using Jenkins, Maven, SonarQube and Nexus for artifact management.

---

## Project Overview

The pipeline automates the following steps:

1. Pull code from GitHub  
2. Build the project using Maven  
3. Perform code quality analysis using SonarQube  
4. Store build artifacts in Nexus Repository  

---

## Tech Stack

- Jenkins – CI/CD automation  
- Maven – Build tool  
- SonarQube – Code quality analysis  
- Nexus Repository – Artifact storage  
- GitHub – Source code management  
- Docker – Containerized services  

---

## Pipeline Flow

GitHub → Jenkins → Maven Build → SonarQube → Nexus

---

## Project Structure

my-app/
├── Jenkinsfile  
├── pom.xml  
├── src/  

---

## Jenkins Pipeline Stages

Build  
Compiles the project using Maven  

SonarQube Analysis  
Analyzes code quality and detects issues  

Artifact Upload (Nexus)  
Uploads build artifact to Nexus repository  

---

## Authentication

GitHub uses Personal Access Token  
SonarQube uses authentication token  
Nexus uses username and password configured in Maven settings.xml  

---

## Artifact Storage

Artifacts are stored in Nexus at:

http://192.168.70.138:8081/repository/releases/

---

## Key Features

- Automated CI/CD pipeline  
- Code quality analysis  
- Artifact storage and versioning  
- Integration of multiple DevOps tools  

---

## How to Run

1. Push code to GitHub  
2. Trigger Jenkins pipeline  
3. Monitor build in Jenkins  
4. View analysis in SonarQube  
5. Verify artifact in Nexus  

---


## Author

Rajat Goel
