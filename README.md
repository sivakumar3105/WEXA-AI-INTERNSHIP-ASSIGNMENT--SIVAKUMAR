# DevOps Internship Assessment – Next.js App Containerization & Deployment

## About this project
This is my DevOps internship assignment. I containerized a **Next.js app** using Docker, set up **GitHub Actions** to automatically build and push the Docker image, and deployed it on **Kubernetes (Minikube)**.  

The Docker image is pushed to **GitHub Container Registry (GHCR)** so anyone can run it locally or in Kubernetes.  

All files like code, Dockerfile, workflow, and Kubernetes manifests are in this repo.

---

## Repo Contents
- **Dockerfile** – for building the Next.js app image  
- **.github/workflows/docker-build.yml** – GitHub Actions workflow  
- **k8s/deployment.yaml** – Kubernetes deployment  
- **k8s/service.yaml** – Kubernetes service  
- **pages/** – Next.js app code  
- **public/** – static assets  
- **package.json** – Node.js dependencies  
- **README.md** – instructions (this file)  

---

## My Environment & Setup (Used for Testing)

**System Details**  
- **Device Name:** SIVALAPTOP  
- **Processor:** 13th Gen Intel(R) Core(TM) i7-13620H (2.40 GHz)  
- **Installed RAM:** 16 GB (15.7 GB usable)  
- **System Type:** 64-bit OS, x64-based processor  
- **Edition:** Windows 11 Home Single Language  
- **Version:** 24H2  
- **Installed on:** 26-04-2025  
- **OS Build:** 26100.6584  
- **Serial Number:** PF573X40  
- **Windows Feature Experience Pack:** 1000.26100.234.0  
   

**Software Versions Used**  
- **Node.js:** v20.x (for running the Next.js app)  
- **npm:** v9.x (package manager for Node.js)  
- **Docker Desktop:** 4.x (with WSL 2 backend)  
- **Docker Engine:** 24.x  
- **Minikube:** v1.30.x (local Kubernetes cluster)  
- **kubectl:** v1.30.x (for managing Kubernetes resources)  
- **Browser for testing:** Chrome / Edge  

**Notes from Testing**  
- This laptop was used to run Docker, Minikube, and test the Next.js app.  
- RAM and CPU were sufficient to run multiple containers and a local Kubernetes cluster smoothly.  
- Building Docker images, pushing to GHCR, and deploying to Minikube were tested and successful.  
- In port 3000  worked correctly.  

---

## Steps I Followed to Run the Project

### 1. Clone the Repo
```bash
git clone https://github.com/sivakumar3105/WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR.git
cd WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR

2. Build and Run Locally Using Docker
docker build -t nextjs-app .
docker run -d -p 3000:3000 nextjs-app
Open your browser at http://localhost:3000
3. GitHub Actions CI/CD
On push to the main branch, the workflow will:
Build the Docker image
Tag the image with latest
Push it to GitHub Container Registry (GHCR):
ghcr.io/sivakumar3105/wexa-ai-internship-assignment/nextjs-app:latest
4. Kubernetes Deployment (Minikube)
Deploy Application
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
Access Application
minikube service nextjs-app
Opens the application in default browser.
Links
GitHub Repository: https://github.com/sivakumar3105/WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR
Docker Image (GHCR): ghcr.io/sivakumar3105/wexa-ai-internship-assignment/nextjs-app:latest

Workflow Diagram:
Code → Docker → GitHub Actions → GHCR → Minikube → Browser
