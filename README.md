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

## 🧰 Tech Stack

| Category | Tools Used |
|-----------|-------------|
| Version Control | Git, GitHub |
| Build Tool | Maven |
| CI/CD | Jenkins |
| Artifact Repository | Nexus |
| Configuration Management | Ansible |
| Provisioning | Terraform |
| Application Server | Apache Tomcat |
| Cloud Platform | AWS |
| Monitoring | Grafana |

---

## ⚙️ Workflow Overview

```mermaid
graph LR
A[Developer commits code to GitHub] --> B[GitHub Webhook triggers Jenkins]
B --> C[Jenkins builds using Maven]
C --> D[Artifacts uploaded to Nexus Repository]
D --> E[Terraform provisions AWS Infrastructure]
E --> F[Ansible deploys app to Tomcat Server]
F --> G[Grafana monitors application performance]
