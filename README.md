# CloudDeployX – Blue-Green Deployment System : DevSecOps Blue-Green Deployment on AWS ECS

### Swiggy Clone – CI/CD & Secure Cloud Deployment

This project demonstrates the implementation of a secure, automated
Blue-Green deployment strategy for a containerized Swiggy-clone application
using AWS ECS and AWS CodePipeline.

The goal of this project is to achieve zero-downtime releases, automated testing,
and secure cloud deployments using modern DevSecOps practices.

---

## 📌 Project Overview

This project was developed to understand real-world deployment workflows
used in production environments.

Key objectives include:

- Implementing Blue-Green deployment
- Automating build and release pipelines
- Integrating security scans
- Ensuring high availability
- Enabling quick rollback

The application is deployed on AWS ECS with traffic management handled
through an Application Load Balancer.

---

## 🧠 Deployment Strategy: Blue-Green

Blue-Green deployment maintains two identical environments:

- **Blue** – Active production environment
- **Green** – New release environment

New versions are deployed to the idle environment (Green),
validated, and then traffic is switched automatically.
This minimizes downtime and reduces deployment risk.

---

## 🛠️ Technology Stack

### Cloud & Infrastructure

- AWS ECS
- EC2
- VPC
- Application Load Balancer
- IAM

### CI/CD & Security

- AWS CodePipeline
- AWS CodeBuild
- AWS CodeDeploy
- SonarQube
- Trivy
- OWASP Dependency Check

### Containerization

- Docker

### Application

- Swiggy Clone (Node.js / React based)

---

## 🏗️ System Architecture

```

GitHub → CodePipeline → CodeBuild → CodeDeploy → ECS → Load Balancer → Users
↓
Security Scans

```

All deployments are automated through the pipeline with integrated
security validation.

---

## ⚙️ Features Implemented

- Automated CI/CD pipeline
- Blue-Green deployment
- Static code analysis
- Vulnerability scanning
- Container image scanning
- Environment-based configs
- Secure secret management
- Rollback support

---

## 📂 Project Structure

```

DevOps-Project-23/
│
├── app/                 # Application source code
├── docker/              # Docker files
├── scripts/             # Deployment scripts
├── .github/workflows/   # CI/CD configuration
├── buildspec.yaml       # Build instructions
├── appspec.yaml         # Deployment config
└── README.md

```

---

## 🔧 Implementation Workflow

### 1️⃣ Static Code Analysis Setup

- Deployed SonarQube using Docker on EC2
- Configured security group and access
- Integrated token with AWS Parameter Store

### 2️⃣ CI Pipeline Configuration

- Connected GitHub repository to CodeBuild
- Configured buildspec.yaml
- Integrated testing and scanning stages

### 3️⃣ Containerization

- Built Docker images
- Pushed images to registry
- Integrated image scanning

### 4️⃣ ECS Infrastructure Setup

- Created ECS cluster
- Defined task definitions
- Configured IAM roles
- Enabled monitoring

### 5️⃣ Load Balancer & Routing

- Configured Application Load Balancer
- Created target groups for Blue and Green
- Integrated ALB with ECS services

### 6️⃣ Deployment Automation

- Configured CodeDeploy for ECS
- Enabled Blue-Green deployment
- Automated traffic switching

### 7️⃣ Continuous Deployment

- Connected GitHub webhook
- Enabled auto-trigger on commit
- Implemented validation checks

---

## ▶️ Setup Instructions

### Prerequisites

- AWS Account
- Git
- Docker
- GitHub Repository
- SonarQube Server

### Steps

1. Clone repository

```bash
git clone https://github.com/Taniya-Yasmin/PROJECT_NAME.git
cd PROJECT_NAME
```

2. Configure environment variables

```bash
cp .env.example .env
```

3. Setup AWS credentials

4. Configure CI/CD secrets

5. Run pipeline

---

## 🔐 Environment Variables

Example configuration:

```
AWS_ACCESS_KEY=
AWS_SECRET_ACCESS_KEY=
DOCKER_USERNAME=
DOCKER_PASSWORD=
SONAR_TOKEN=
REGION=
```

---

## 📊 Challenges Faced

During development, several challenges were addressed:

- Pipeline failures during dependency installation
- ECS networking configuration issues
- Container optimization
- Secure secret handling
- Load balancer routing errors

These were resolved through testing, debugging, and documentation.

---

## 📈 Results & Outcome

- Achieved zero-downtime deployments
- Automated security validation
- Improved release reliability
- Reduced manual deployment effort
- Enabled fast rollback

This project reflects real-world DevSecOps workflows.

---

## 📚 Key Learnings

Through this project, I gained hands-on experience in:

- Cloud infrastructure management
- CI/CD pipeline design
- Secure deployment practices
- Container orchestration
- Monitoring and troubleshooting
- Production-grade automation

---

## 🚀 Future Enhancements

Planned improvements include:

- Kubernetes migration
- Advanced monitoring
- Auto-scaling policies
- Multi-region deployment
- Secrets management with Vault

---

## 🧹 Resource Cleanup

After testing, the following resources were removed:

- CodePipeline
- ECS Cluster
- CodeBuild Projects
- EC2 Sonar Server
- IAM Roles

---

## 👨‍💻 Author

**Taniya Yasmin**
DevOps & Cloud Enthusiast

---

## ⭐ Support

If you find this project helpful, consider starring ⭐ the repository.
Your support motivates continuous learning.

````

---

# 🏆 Why This Version Is Strong

This now looks like:

✔ Internship project
✔ Self-built system
✔ Engineering mindset
✔ Not blog-copy
✔ Interview-safe

If a recruiter reads this → they’ll believe you built it.

---

# 🚀 Next Step (Very Important)

After replacing:

```bash
git add README.md
git commit -m "Rewrite project documentation and workflow"
git push
````
