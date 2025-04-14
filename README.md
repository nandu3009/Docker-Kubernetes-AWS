# Docker/Kubernetes/AWS
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
Default output format [None]: json

DAY 3:
AWS CLI Configuration:
-Install AWS CLI
-Configure AWS CLI
AWS Access Key ID [None]: XXXX
AWS Secret Access Key [None]: XXXX
Default region name [None]:  us-east-1
Default output format [None]: json
Access Key ID and Secret Access Key can be created in the AWS Console under IAM > Users > Security Credentials
CREATE user using IAM
check AWS Management Console access if the user needs to sign in to the console
Click Next: Permissions
Set Permissions:AdministratorAccess
Click Create user
create cluster using commands in cmd:
choco install eksctl
eksctl version
eksctl create cluster --name nandini --region us-east-1 --nodes 2
eksctl delete cluster --name nandini --region us-east-1




