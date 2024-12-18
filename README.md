# Kidney-Disease-Classification-MLflow-DVC

## **Workflows**
1. Update `config.yaml`
2. Update `secrets.yaml` (Optional)
3. Update `params.yaml`
4. Update the entity
5. Update the configuration manager in `src/config`
6. Update the components
7. Update the pipeline
8. Update the `main.py`
9. Update the `dvc.yaml`
10. Update the `app.py`

---

## **How to Run?**

### **Steps**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/krishnaik06/Kidney-Disease-Classification-Deep-Learning-Project
Create a Conda Environment

bash
Copy code
conda create -n cnncls python=3.8 -y
conda activate cnncls
Install the Requirements

bash
Copy code
pip install -r requirements.txt
Run the Application

bash
Copy code
python app.py
Open Your Localhost and Port

MLflow
Documentation
MLflow Tutorial
Commands:

Start MLflow UI:
bash
Copy code
mlflow ui
Dagshub Integration
Set environment variables for tracking MLflow experiments using Dagshub:

bash
Copy code
export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Kidney-Disease-Classification-MLflow-DVC.mlflow
export MLFLOW_TRACKING_USERNAME=entbappy
export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0
Run the script:

bash
Copy code
python script.py
DVC Commands
Initialize DVC:

bash
Copy code
dvc init
Reproduce the pipeline:

bash
Copy code
dvc repro
View the DAG:

bash
Copy code
dvc dag
About MLflow & DVC
MLflow
Production-grade tool.
Tracks all experiments.
Logs and tags models.
DVC
Lightweight experiment tracker (suitable for POCs).
Helps in creating and orchestrating pipelines.
AWS-CICD-Deployment-with-Github-Actions
Steps for Deployment
Login to AWS Console.

Create IAM User for Deployment:

Access Required:
EC2 Access: Virtual machine access.
ECR Access: Elastic Container Registry to save Docker images.
Deployment Workflow
Build the Docker image of the source code.
Push the Docker image to ECR.
Launch an EC2 instance.
Pull the Docker image from ECR on EC2.
Launch the Docker container in EC2.
IAM Policies
AmazonEC2ContainerRegistryFullAccess
AmazonEC2FullAccess
Steps for AWS Deployment
Create ECR Repository:

Save the URI:
bash
Copy code
566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken
Create EC2 Instance (Ubuntu).

Install Docker in EC2 Machine (Optional):

bash
Copy code
sudo apt-get update -y
sudo apt-get upgrade
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
Configure EC2 as a Self-Hosted Runner:

Go to Settings > Actions > Runner > New Self-Hosted Runner.
Choose OS and run the provided commands one by one.
Setup GitHub Secrets:

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=566373416292.dkr.ecr.ap-south-1.amazonaws.com
ECR_REPOSITORY_NAME=simple-app
Project Description
This project classifies kidney disease using MLflow and DVC. The pipeline includes creating and deploying Dockerized models with AWS CICD integration.

