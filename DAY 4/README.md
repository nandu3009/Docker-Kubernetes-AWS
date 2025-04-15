#Objective:
To create an S3 bucket and deploy a Lambda function in AWS using a Python script.

-Step 1: Create an S3 Bucket

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
