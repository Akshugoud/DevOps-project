# 🚀 DevOps Project  
### **Web Application Deployment using CI/CD in Monolithic Architecture**

---

## 🧾 About the Project

This project demonstrates a **complete DevOps pipeline** for deploying a monolithic web application using a fully automated CI/CD process.  
It integrates multiple tools for source control, build automation, configuration management, provisioning, deployment, and monitoring.

---

## 🛠️ Key Features

- **Infrastructure Provisioning:** Automated AWS infrastructure setup using **Terraform** within a Jenkins pipeline.  
- **Jenkins Master-Slave Setup:** Configured distributed Jenkins environment for parallel and efficient CI/CD execution.  
- **Build Automation:** Used **Maven** to build the Java application and publish artifacts to **Nexus Repository**.  
- **Deployment Automation:** Deployed the application to **Apache Tomcat** using **Ansible Playbooks**.  
- **Continuous Integration:** Configured **GitHub Webhooks** to trigger Jenkins jobs automatically upon code commits.  
- **Monitoring:** Integrated **Grafana** for real-time system and application performance monitoring.  

---

## ⚙️ Tools and Technologies Used

| Category | Tools |
|-----------|--------|
| **Cloud Platform** | AWS |
| **Infrastructure as Code (IaC)** | Terraform |
| **Version Control** | Git, GitHub |
| **CI/CD** | Jenkins |
| **Configuration Management** | Ansible |
| **Artifact Storage** | Amazon S3 |
| **Application Server** | Apache Tomcat |
| **Code Quality Analysis** | SonarQube |
| **Monitoring** | Prometheus, Grafana |


---

## ⚙️ Workflow Overview

```mermaid
graph LR
A[Developer commits code to GitHub] --> B[GitHub Webhook triggers Jenkins]
B --> C[Build Stage - Jenkins uses Maven to build the application]
C --> D[Test Stage - Automated testing in Jenkins]
D --> E[Code Quality Check - SonarQube analysis]
E --> F[Artifact Stage - WAR file generated and versioned]
F --> G[S3 Upload - Artifact stored for rollback/version control]
G --> H[Deployment Stage - Ansible deploys app to Tomcat server]
H --> I[Slack Notification - Team notified about deployment status]
I --> J[Monitoring - Grafana and Prometheus track system health]

