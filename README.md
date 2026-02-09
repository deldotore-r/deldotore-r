# Reinaldo Del Dotore
### Cloud Infrastructure | DevOps | SRE

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Reinaldo_Del_Dotore-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/reinaldo-del-dotore/)
[![Email](https://img.shields.io/badge/Email-Contato-D14836?style=flat&logo=gmail&logoColor=white)](mailto:deldotore@gmail.com)
[![Website](https://img.shields.io/badge/Portfolio-deldotore.com-0ea5e9?style=flat&logo=google-cloud)](https://deldotore.com)

---

## 👨‍💻 Professional Profile

Infrastructure professional transitioning in a structured manner to **DevOps and SRE**, with **30 years of experience in mission-critical and highly regulated environments**. My background was built in contexts where **operational discipline, reliability, traceability, and rigorous technical documentation** are not differentiators — they are mandatory.

I am currently focused on designing and operating **resilient cloud architectures**, **automating CI/CD pipelines**, **Infrastructure as Code (IaC)**, and **observability**, always prioritizing operational predictability, security, and risk reduction.

---

## 🛠️ Technical Expertise

- **Cloud (AWS):** S3, CloudFront, IAM, VPC, EC2.
- **Infrastructure as Code:** Terraform (modular structure, versioning, reproducibility).
- **CI/CD:** GitHub Actions, GitLab CI/CD.
- **Containers:** Docker, Docker Compose.
- **Linux:** Debian-based systems administration (Ubuntu/Xubuntu), Bash scripting.
- **Automation:** Python for operational scripts and task automation.
- **Observability (active study):** Prometheus, Grafana.

---

## 🚀 Featured Projects

### 🌐 Full CI/CD Pipeline — **deldotore.com**
🔗 https://github.com/deldotore-r/deldotore_site

**Focus:** *Continuous Deployment, Cloud Networking & Security*

End-to-end continuous delivery pipeline for my personal portfolio.

- **Serverless architecture** using **Amazon S3 + CloudFront (CDN)**.
- **GitHub Actions** pipeline with automated deployment, programmatic cache invalidation, and secure *secrets* management.
- **IAM policies** enforcing *Least Privilege*.
- Architecture designed for operational simplicity and low cost.

---

### 🏗️ AWS Infrastructure with Terraform
🔗 https://github.com/deldotore-r/rotary-infra-aws

**Focus:** *Infrastructure as Code (IaC) & Standardization*

Automated provisioning of foundational AWS infrastructure.

- Reproducible definition of **VPC, Subnets, and Security Groups**.
- **EC2** instance deployment fully managed via code.
- Clear separation of `main.tf`, `variables.tf`, and `outputs.tf`.
- Strong emphasis on version control, readability, and change management.

---

### 💶 Airflow Exchange Rate Pipeline — **EUR / BRL**
🔗 https://gitlab.com/deldotore-r/airflow-cambio-pipeline

**Focus:** *Data Engineering, Orchestration & Automated Publishing*

Automated data pipeline that monitors the **EUR/BRL exchange rate**, covering business hours in **Portugal and Brazil**. The architecture emphasizes scalability, process decoupling, and fully automated publication of results.

**Architecture & Data Flow**

- **Ingestion (Extract):** A dedicated DAG collects data from **AwesomeAPI** every 5 minutes between **09:00 (Lisbon)** and **18:00 (Brasília / 21:00 Lisbon)**, persisting the data into a CSV dataset.
- **Processing & Visualization (Transform / Load):** A second, independent DAG processes the data daily using **Pandas** and **Plotly**, generating an interactive HTML dashboard.
- **Automated Deploy (CI/CD):** The generated report is pushed via Git, triggering a **GitLab CI/CD** pipeline that publishes the dashboard to **GitLab Pages**.

**Technologies**

- **Orchestration:** Apache Airflow 2.8.1 (LocalExecutor)
- **Containerization:** Docker & Docker Compose
- **Language:** Python 3.11
- **Libraries:** Pandas, Plotly, Pendulum (timezone management)
- **Infrastructure:** PostgreSQL (Airflow metadatabase), GitLab CI/CD, GitLab Pages

**Technical Highlights**

- **Decoupled DAGs:** Clear separation between high-frequency ingestion and batch reporting, improving resilience and resource efficiency.
- **Secure Automation with Deploy Keys:** Exclusive SSH deploy keys mapped into Docker volumes, enabling secure and automated `git push` operations without exposing personal credentials.
- **Timezone Management:** Robust configuration using **Pendulum** to synchronize workflows across Lisbon and Brasília timezones.
- **Custom Health Checks:** Docker container health monitoring based on internal **Airflow SchedulerJob** processes.

**Live Dashboard**

🔗 Access the Exchange Rate Dashboard on GitLab Pages

---

### 🐳 Airflow Pipeline with Docker Compose
🔗 https://github.com/deldotore-r/airflow-cambio-pipeline

**Focus:** *Containers, Local Orchestration & Data Pipelines*

Local **Apache Airflow** environment built with **Docker Compose**, aimed at hands-on studies of pipeline orchestration.

- Containerized stack with isolated services configured via environment variables.
- Troubleshooting and resolution of real-world issues related to **permissions, health checks, and service initialization**.
- Strong focus on operational understanding of containers, beyond superficial usage.

---

### 💾 Smart Backup for WSL / Linux
🔗 https://github.com/deldotore-r/smart-backup-wsl

**Focus:** *Linux Automation & Operational Efficiency*

**Bash** script for intelligent backup automation in development environments.

- Smart exclusion of irrelevant directories (`node_modules`, `.terraform`, caches, etc.).
- Implementation of **controlled retention policies** and **execution logging**.
- Backup volume reduction exceeding **90%** in lab environments.

---

## 📊 Observability — Ongoing Studies

Hands-on project under development using **Prometheus + Grafana**, focused on:

- Service and system metrics collection.
- Dashboard creation and operational visualization.
- Introduction to alerting and SLI/SLO concepts.

---

## 📚 Roadmap & Active Studies (2026)

- **Containers & Orchestration:** Docker (advanced) and Kubernetes (K8s).
- **Observability:** Prometheus, Grafana, and SRE fundamentals.
- **CI/CD:** More advanced pipelines and deployment strategies.
- **Certifications:** Preparation for **AWS Cloud Practitioner** and **AWS Solutions Architect**.

---

*Reinaldo Del Dotore © 2026*

