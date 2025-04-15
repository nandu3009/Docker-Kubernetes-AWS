-Create a Docker Image for Kubernetes

-Create a simple app (e.g., Python, Node.js, Go). Example: Python Flask 

-Test the **Create a Kubernetes Deployment Using the Image**
-deployment.yaml
-Expose the App
-service.yaml
Apply the service:

-kubectl apply -f service.yaml
-Access the Application

Check the external IP:

-kubectl get service flask-service

Open the external IP in your browser to access the app.

output:file:Scrape.csv
