# End-to-End DevOps Project: Pacman App

## About This Project

This project involved taking a 'Pacman' web application through a full cloud-native lifecycle. I was responsible for containerizing the app, building automated CI/CD pipelines, deploying it to Kubernetes, and setting up the necessary infrastructure, monitoring, and logging.

## Key Technical Implementations

* **Containerization:**
    * Wrote a multi-stage **Dockerfile** for the application.
    * Created a **`docker-compose.yaml`** to run the app and a **MongoDB** database locally for testing.

* **CI/CD Pipelines:**
    * Built automated CI/CD pipelines in **Azure DevOps**, **GitLab CI**, and **Jenkins**.
    * Pipelines were configured to **build**, **test**, **tag**, and **push** Docker images to a private registry.
    * Added a "Deploy" stage to automatically apply Kubernetes manifests.

* **Kubernetes Deployment:**
    * Wrote all K8s manifests: `Namespace`, `Deployment`, `Service`, and `PersistentVolumeClaim` (for MongoDB).
    * Configured an **Ingress** controller to expose the application to a public DNS.
    * Implemented a **GitOps** workflow using **ArgoCD** to sync cluster state with a Git repository.

* **Infrastructure as Code (IaC) & Monitoring:**
    * Used **Terraform** to provision an **Azure VM** (B-Series) as a new K8s worker node.
    * Used **Ansible** to automatically configure the node (installing `kubectl`, `docker`, etc.).
    * Deployed **Prometheus** & **Grafana** for metrics and **EFK Stack** for logging.

## Technologies Used

* **Containerization:** Docker, Docker Compose
* **Orchestration:** Kubernetes
* **CI/CD:** Azure DevOps, GitLab CI, Jenkins
* **GitOps:** ArgoCD
* **IaC:** Terraform, Ansible
* **Database:** MongoDB
* **Monitoring:** Prometheus, Grafana
* **Logging:** EFK Stack (Elasticsearch, Fluentd, Kibana)
