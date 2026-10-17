# Reinaldo Del Dotore
### Data Platform Engineer | Kubernetes | Airflow | Spark | AWS
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Reinaldo_Del_Dotore-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/reinaldo-del-dotore/)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat&logo=gmail&logoColor=white)](mailto:deldotore@gmail.com)
[![Website](https://img.shields.io/badge/Portfolio-deldotore.com-0ea5e9?style=flat&logo=google-cloud)](https://deldotore.com)

---

## 👨‍💻 Professional Profile

Data Platform Engineer at **COCUS Portugal** since March 2026, on a small team that owns the infrastructure of a production analytics platform on **Amazon EKS**: Airflow, Spark on Kubernetes, Apache Iceberg, Hive Metastore, Dremio, NiFi, RisingWave and Amazon EMR.

My work centers on **incident triage, root-cause investigation and operational tooling**: finding out why something broke, proving it with evidence, and writing it down so the next person doesn't start from zero. Before IT, I served 30 years as an officer in the São Paulo Military Police, where **operational discipline, process rigor and documentation** were part of the job.

---

## 🛠️ Technical Expertise

**In production, daily:**
* **Kubernetes:** Amazon EKS, kubectl, scheduling, autoscaling, persistent volumes and troubleshooting.
* **Data platform:** Apache Airflow 2.8, Spark on Kubernetes, Apache Iceberg, Hive Metastore, Dremio, NiFi, RisingWave.
* **AWS:** EKS, EMR, S3, IAM, CloudWatch Logs.
* **Observability:** Prometheus, Grafana.
* **Tooling:** Python, Bash and SQL for operations scripts and audits.

**Labs and personal projects:**
* **IaC & CI/CD:** Terraform, GitHub Actions, GitLab CI/CD.
* **Containers:** Docker, Docker Compose, Kubernetes (Kind).
* **Linux:** Ubuntu and Fedora, shell scripting (Bash).

---

## 🏭 Selected Production Work

*Details are generalized and figures rounded to respect client confidentiality.*

### 🧊 Ingestion tasks taking hours, with no errors
A pipeline kept reporting success while tasks that should take minutes ran for more than four hours. Two years of tiny commits without snapshot expiration had grown the table's **Apache Iceberg** metadata to more than 5,000 times the size of its data.
- **Evidence:** Iceberg metadata read directly from S3, commit process sampled through `/proc`, commit counts matched against run history in the Airflow metadata database.
- **Result:** Root cause confirmed; investigation report and remediation plan; a follow-up scan found dozens of tables with the same pattern.

### 🌐 Spark jobs failing seconds after landing on a new node
Bursts of Spark drivers failed with network timeouts whenever the cluster scaled up. New nodes reported Ready in about 13 seconds, but pod networking took 2 to 3.5 minutes to converge.
- **Evidence:** Live measurements of new nodes and EKS API server audit logs.
- **Result:** Root cause confirmed; four mitigation options documented for the platform decision.

### 🧹 Daily platform audit
A written morning protocol of 21 checks, backed by a dependency-free **Python** CLI (kubectl and AWS CLI only) that finds waste and stuck work across environments: crash-looping and OOM-killed pods, zombie Spark pods, orphaned EMR clusters, stuck DAG runs and orphaned Hive Metastore locks.
- **Result:** Found, among other things, idle EMR clusters with 18 instances and no auto-termination.

---

## 🚀 Featured Projects

### 📊 [Airflow Monitoring Stack (Prometheus & Grafana)](https://github.com/deldotore-r/airflow-monitoring-stack)
**Focus:** *Observability*

Monitoring stack for Apache Airflow: Airflow sends StatsD metrics to an exporter scraped by **Prometheus**, and **Grafana** shows scheduler heartbeat, task throughput and task latency.
- Value mapping for an online/offline scheduler heartbeat panel.
- Task latency from `rate()` over duration sums and counts, instead of historical averages.
- Runs locally with **Docker Compose**.

### 💶 [Airflow Exchange Rate Pipeline – EUR/BRL](https://gitlab.com/deldotore-r/airflow-cambio-pipeline)
**Focus:** *Data Engineering, Orchestration & Automated Publishing*

Automated data pipeline monitoring the **EUR/BRL exchange rate**, covering business hours in **Portugal and Brazil**.

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

### 🐳 [Kubernetes Local Automation with Kind](https://github.com/deldotore-r/kubernetes_01)
**Focus:** *Container Orchestration & Automation*

Local Kubernetes environment using **Kind**, with complete automation via **Bash scripts**.
- **"One-Command-Setup":** Bash script prepares the cluster, manages permissions and deploys the application.
- **Resource management:** 2 Nginx replicas with `limits` and `requests`.
- **Service Discovery:** Exposure via Service (ClusterIP) with Port-Forward.
- Clear layer separation (k8s vs scripts) and a cleanup script.

### 🌐 [Full CI/CD Pipeline: deldotore.com](https://github.com/deldotore-r/deldotore_site)
**Focus:** *Continuous Deployment*

Automated delivery pipeline for my personal website.
- Static site on **S3** behind **CloudFront**.
- **GitHub Actions** pipeline with programmatic cache invalidation and secrets management.
- Restricted **IAM** policies (least privilege).

### Other repositories
- [AWS Basic Infrastructure with Terraform](https://github.com/deldotore-r/aws-basic-infra-terraform): EC2, Security Groups and S3 through the full `init` to `destroy` cycle.
- [Smart Backup for WSL/Linux](https://github.com/deldotore-r/smart-backup-wsl): shell-script backups with exclusion rules, retention and logs, compatible with `cron`.

---

## 📚 Roadmap & Active Studies (2026)

* **Kubernetes:** Preparing for the Certified Kubernetes Administrator (CKA) exam.
* **Apache Iceberg:** Internals and concurrency model.
* **dbt:** Fundamentals, toward analytics engineering.
* **Next:** Spark performance tuning and AWS Certified Data Engineer – Associate.

---

*Reinaldo Del Dotore © 2026*
