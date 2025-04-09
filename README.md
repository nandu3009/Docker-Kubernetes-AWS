# Docker-Kubernetes
DAY 1:
Install Docker and VS Code extensions.
- Set up a basic Python project with Docker.
- Build and run your first Docker image inside VS Code
- COMMANDS:
- docker build -t testfile .
- docker run testfile
- docker run -d -p 8000:8000

DAY 2:
COMMANDS:
minikube start
kubectl get nodes
kubectl apply -f deployment.yaml
docker build -t book-scraper:latest .
minikube start
minikube docker-env | Invoke-Expression  
docker build -t book-scraper:latest .
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get pods

minikube service book-scraper-service 

