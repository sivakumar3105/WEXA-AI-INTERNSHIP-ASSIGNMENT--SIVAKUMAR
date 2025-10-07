# WEXA AI DevOps Internship Assignment - Siva Kumar

This is a simple Next.js application that I containerized using Docker, automated with GitHub Actions, and deployed on Minikube (Kubernetes).

## 1. Run Locally
```
git clone https://github.com/sivakumar3105/WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR.git
cd WEXA-AI-INTERNSHIP-ASSIGNMENT--SIVAKUMAR
npm install
npm run dev
```

## 2. Docker Build and Run
```
docker build -t nextjs-app .
docker run -p 3000:3000 nextjs-app
```

## 3. GitHub Actions
Push to main triggers build and push to GHCR:
`ghcr.io/sivakumar3105/wexa-ai-internship-assignment--sivakumar:latest`

## 4. Deploy on Minikube
```
minikube start
kubectl apply -f k8s/
kubectl get pods
kubectl get svc
minikube service nextjs-service
```

**Author:** Siva Kumar
