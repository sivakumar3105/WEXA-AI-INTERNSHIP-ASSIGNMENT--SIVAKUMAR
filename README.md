\# DevOps Internship Assessment – Next.js Containerization \& Deployment



\## Project Summary

This project demonstrates the \*\*containerization and deployment of a Next.js application\*\* using Docker, automated CI/CD with GitHub Actions, and deployment to Kubernetes using Minikube. The Docker image is published on \*\*GitHub Container Registry (GHCR)\*\*, allowing the application to be run locally or in a Kubernetes cluster. The repository includes all source code, Dockerfile, GitHub Actions workflow, and Kubernetes manifests, along with step-by-step instructions for setup and deployment.



---



\## Project Overview

This repository contains a \*\*Next.js application\*\* that has been fully containerized and automated for deployment. The workflow covers:



\- Docker containerization with best practices  

\- Automated CI/CD using GitHub Actions and GHCR  

\- Deployment on Kubernetes (Minikube)  

\- Complete documentation for setup, running, and verification  



---



\## Objectives

\- Containerize a Next.js application following best practices  

\- Automate Docker image build and push to \*\*GHCR\*\* using GitHub Actions  

\- Deploy the containerized application to \*\*Kubernetes\*\* using Minikube  

\- Provide clear documentation and instructions for local setup, container usage, and deployment  



---



\## Repository Structure



├── Dockerfile # Docker configuration for Next.js app

├── .github/

│ └── workflows/

│ └── docker-build.yml # GitHub Actions workflow for CI/CD

├── k8s/

│ ├── deployment.yaml # Kubernetes deployment manifest

│ └── service.yaml # Kubernetes service manifest

├── pages/ # Next.js application source code

├── public/ # Static assets

├── package.json # Node.js dependencies

└── README.md # Project documentation

---



\## Setup Instructions



\### 1. Clone the Repository

```bash

git clone https://github.com/sivakumar3105/WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR.git

cd WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR



2\. Build and Run Locally Using Docker

docker build -t nextjs-app .

docker run -d -p 3000:3000 nextjs-app





Open your browser at http://localhost:3000



3\. GitHub Actions CI/CD



On push to the main branch, the workflow will:



Build the Docker image



Tag the image with latest



Push it to GitHub Container Registry (GHCR):



ghcr.io/sivakumar3105/wexa-ai-internship-assignment/nextjs-app:latest



4\. Kubernetes Deployment (Minikube)

Deploy Application

kubectl apply -f k8s/deployment.yaml

kubectl apply -f k8s/service.yaml



Access Application

minikube service nextjs-app





Opens the application in your default browser.



5\. Optional: Port Conflicts



If port 3000 is already in use, run on an alternative port:



docker run -d -p 3001:3000 ghcr.io/sivakumar3105/wexa-ai-internship-assignment/nextjs-app:latest





Access via http://localhost:3001

Links



GitHub Repository: https://github.com/sivakumar3105/WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR



Docker Image (GHCR): ghcr.io/sivakumar3105/wexa-ai-internship-assignment/nextjs-app:latest

