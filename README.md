# Docker/Kubernetes/AWS
DAY 1:
Install Docker and VS Code extensions.
- Set up a basic Python project with Docker.
- Build and run your first Docker image inside VS Code
- COMMANDS:
- docker build -t testfile .
- docker run testfile
- docker run -d -p 8000:8000
![container (1)](https://github.com/user-attachments/assets/3b9b5b49-417f-484a-9f89-53cb34a58040)







![docker image](https://github.com/user-attachments/assets/d25e5b5c-78a2-4f94-ae41-e55ac2158965)



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


DAY 4:AWS Project Setup: S3 Bucket + Lambda Function Using Python

#Objective:
To create an S3 bucket and deploy a Lambda function in AWS using a Python script.

📁 Step 1: Create an S3 Bucket

1. Go to the **S3 Console**:  
   Navigate to: `https://console.aws.amazon.com/s3/`.

2. Click on **"Create bucket"**.

3. Provide a **unique bucket name**.  
   _Example used_: `utfyudgigjchighjghh`

4. Select the **AWS Region**.  
   _Example used_: `Asia Pacific (Mumbai) - ap-south-1`

5. Leave other settings default (or configure as per your use case):
  
6. Click **"Create bucket"**.

7. Confirmation will appear: ✅  
   “Successfully created bucket…”

Step 2: Create a Lambda Function

1. Navigate to the **Lambda Console**:  
   URL: `https://console.aws.amazon.com/lambda/`

2. Click **"Create function"**.

3. Choose:
   - **Author from scratch**
   - Function name: _e.g., `nandini`_
   - Runtime: `Python 3.x` (e.g., Python 3.12)

4. Create or choose an **IAM role** with the following permissions:
   - Basic Lambda execution
   - (Optional) Access to S3 if needed for integration

5. Click **"Create function"**.

6. After creation, you'll see:
   - A **function ARN**
   - An empty editor with the option to edit/upload code

Step 3: Upload Python Code to Lambda

1. In the function editor, click on **"Code"** tab.

2. Add or upload your Python script.  
   Example `lambda_function.py` content:

   ```python
   def lambda_handler(event, context):
       name = event.get("name", "Guest")
       return f"Hello, {name}!"
   ```

3. Click **Deploy** to save and activate your code.
   
4.Step 4: Test the Lambda Function

1. Go to the **Test** tab.

2. Click **Create new test event**.

3. Example event:

   ```json
   {
     "name": "Alice"
   }
   ```

4. Click **Test**.

5. Output:
   ```
   "Hello, Alice!"
   ```



DAY 5:










