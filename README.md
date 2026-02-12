# Reinaldo Del Dotore
### Cloud Infrastructure | DevOps | SRE
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Reinaldo_Del_Dotore-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/reinaldo-del-dotore/)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat&logo=gmail&logoColor=white)](mailto:deldotore@gmail.com)
[![Website](https://img.shields.io/badge/Portfolio-deldotore.com-0ea5e9?style=flat&logo=google-cloud)](https://deldotore.com)

---

## 👨‍💻 Professional Profile

IT infrastructure professional transitioning to **DevOps and SRE**. I bring three decades of experience in critical and highly regulated environments, where **operational discipline, process rigor, and technical documentation** are the pillars of mission success.

Currently focused on building resilient cloud architectures, automating delivery cycles (CI/CD), and managing infrastructure as code (IaC), always prioritizing security and operational predictability.

---

## 🛠️ Technical Expertise

* **Cloud:** AWS (S3, CloudFront, IAM, VPC, EC2).
* **Infrastructure as Code:** Terraform.
* **CI/CD:** GitHub Actions, GitLab CI/CD.
* **Containers & Orchestration:** Docker, Docker Compose, Kubernetes (Kind).
* **Data Orchestration:** Apache Airflow.
* **Linux:** Debian-based systems administration (Ubuntu/Xubuntu), Shell Scripting (Bash).
* **Automation:** Python (Pandas, Plotly, Pendulum) for data pipelines and operational scripts.

---

## 🚀 Featured Projects

### 💶 [Airflow Exchange Rate Pipeline – EUR/BRL](https://gitlab.com/deldotore-r/airflow-cambio-pipeline)
**Focus:** *Data Engineering, Orchestration & Automated Publishing*

Automated data pipeline monitoring the **EUR/BRL exchange rate**, covering business hours in **Portugal and Brazil**. Architecture focused on scalability, process decoupling, and fully automated publishing.

**Architecture & Data Flow:**
- **Ingestion (Extract):** Dedicated DAG collects data from **AwesomeAPI** every 5 minutes between **09:00 (Lisbon)** and **18:00 (Brasília / 21:00 Lisbon)**, persisting to CSV dataset.
- **Processing & Visualization (Transform/Load):** Independent DAG processes data daily using **Pandas** and **Plotly**, generating interactive HTML dashboard.
- **Automated Deploy (CI/CD):** Generated report is published via Git, triggering **GitLab CI/CD** pipeline that publishes to **GitLab Pages**.

**Tech Stack:**
- Apache Airflow 2.8.1 (LocalExecutor), Docker & Docker Compose
- Python 3.11, Pandas, Plotly, Pendulum (timezone management)
- PostgreSQL (Airflow metadatabase), GitLab CI/CD, GitLab Pages

**Technical Highlights:**
- **Decoupled DAGs:** Clear separation between high-frequency ingestion and batch reporting, improving resilience and resource efficiency.
- **Secure Automation with Deploy Keys:** Exclusive SSH keys mapped in Docker volumes, enabling automated `git push` without exposing personal credentials.
- **Timezone Management:** Robust configuration using **Pendulum** to synchronize workflows between Lisbon and Brasília.
- **Custom Health Checks:** Container health monitoring based on internal **Airflow SchedulerJob** processes.

### 🌐 [Full CI/CD Pipeline: deldotore.com](https://github.com/deldotore-r/deldotore_site)
**Focus:** *Continuous Deployment & Cloud Networking*

Automated delivery pipeline for my personal portfolio.
- Serverless architecture using **S3** and **CloudFront CDN**.
- **GitHub Actions** pipeline with programmatic cache invalidation and secrets management.
- Security implementation via restricted **IAM** policies (Least Privilege).
- 31 commits demonstrating iterative evolution and continuous improvements.

### 🏗️ [AWS Self-Healing Web Server (IaC)](https://github.com/deldotore-r/rotary-infra-aws)
**Focus:** *Infrastructure as Code & Cloud Security*

Automated AWS infrastructure provisioning for the Rotary Club da Guarda institutional website.
- **Complete VPC** with public subnets, Internet Gateway, and Route Tables.
- **Security Groups** with dynamic rules: SSH restricted to administrator's IP (obtained via `data "http"`).
- **EC2 with user_data.sh:** Automated deployment via `git clone` and Nginx configuration.
- **S3 Backend** with versioning, encryption, and native locking (no DynamoDB).
- **Elastic IP** for fixed public address.
- Clear demonstration of complete infrastructure bootstrapping.

### 🐳 [Kubernetes Local Automation with Kind](https://github.com/deldotore-r/kubernetes_01)
**Focus:** *Container Orchestration & Automation*

Microservices orchestration in local Kubernetes environment using **Kind** and complete automation via **Bash Scripts**.
- **"One-Command-Setup":** Bash script prepares cluster, manages permissions, and deployments.
- **High Availability:** 2 Nginx replicas with `limits` and `requests` configuration.
- **Service Discovery:** Exposure via Service (ClusterIP) with Port-Forward.
- Clear layer separation (k8s vs scripts) and cleanup script.

### 🔧 [AWS Basic Infrastructure with Terraform](https://github.com/deldotore-r/aws-basic-infra-terraform)
**Focus:** *IaC Fundamentals & Best Practices*

Basic AWS infrastructure for learning, with complete visual documentation.
- Provisioning of **EC2, Security Groups, and S3**.
- Parameterized variables via `terraform.tfvars`.
- Screenshots of complete cycle: `init`, `validate`, `plan`, `apply`, `destroy`.
- Visual confirmation in AWS Console before and after destroy.

### 🔄 [GitLab CI/CD – Static Site Deployment](https://github.com/deldotore-r/gitlab)
**Focus:** *CI/CD Pipeline & GitLab Automation*

GitLab CI/CD pipeline demonstration for automated static site build and deployment.
- **2-stage Pipeline:** Build (validation and artifacts) and Deploy (main branch only).
- **Docker** for process containerization.
- Focus on versioning best practices and automated processes.

### 💾 [Smart Backup for WSL/Linux](https://github.com/deldotore-r/smart-backup-wsl)
**Focus:** *Linux Automation & Efficiency*

Shell Script solution for backup automation in development environments.
- Intelligent exclusion logic (ignores `node_modules`, `.terraform`, etc.) for storage optimization.
- Implementation of controlled retention and execution logs.
- Backup volume reduction over 90% in local labs.
- Compatible with `cron` for periodic executions.

---

## 📚 Roadmap & Active Studies (2026)

* **Containers & Orchestration:** Deep dive into Kubernetes (K8s) and Helm.
* **Observability:** Monitoring with Prometheus and Grafana.
* **Data Engineering:** Expansion of Airflow pipelines with database integration.
* **Certification:** Preparing for AWS Solutions Architect Associate.
* **DevSecOps:** Integration of security practices in CI/CD pipelines.

---

*Reinaldo Del Dotore © 2026*
