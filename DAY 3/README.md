 AWS Config & EKS Cluster Creation
-Step 1: Install Required Tools

Install the following:

-AWS CLI
-eksctl (EKS CLI Tool)
-kubectl

- Step 2: Configure AWS CLI

Commands:
aws configure


It will ask:

- AWS Access Key ID
- AWS Secret Access Key
- Default region (e.g., `us-west-2`)
- Output format (e.g., `json`)


- Step 3: Create the EKS Cluster

You can create a cluster with a single command using `eksctl`.

- Creates EKS cluster and control plane
- Sets up worker nodes
  
It takes ~10–15 minutes.

-Step 4: Verify the Cluster


kubectl get nodes
You should see your EC2 worker nodes in `Ready` state.

Once the external IP is ready, access it in.
cluster will be created in AWS.
