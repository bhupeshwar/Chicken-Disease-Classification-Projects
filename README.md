# Chicken-Disease-Classification-Projects


## Workflows
1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the dvc.yaml (MLOps)


# How to run?

STEPS:

Clone the repository


<code> https://github.com/bhupeshwar/Chicken-Disease-Classification-Projects</code>

 STEP 01- Create a conda environment after opening the repository

<code>conda create -n cnncls python=3.8 -y</code>

<code>conda activate cnncls</code>

 STEP 02- install the requirements

<code>pip install -r requirements.txt</code>

<code>
# Finally run the following command
python app.py
</code>

Now,

<code> open up you local host and port </code>


DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


Note :

DVC (Data Version Control), is essentially an experiment management tool for ML projects. DVC software is built upon Git and its main goal is to codify data, models and pipelines through the command line.


# AWS-CICD-Deployment-with-Github-Actions

1. Login to AWS console.

2. Create IAM user for deployment

<code>
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

</code>

3. Create ECR repo to store/save docker image

<code> - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken </code>

4. Create EC2 machine (Ubuntu)

5. Open EC2 and Install docker in EC2 Machine:

<code>
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker

</code>

6. Configure EC2 as self-hosted runner:


<code>setting>actions>runner>new self hosted runner> choose os> then run command one by one </code>


7. Setup github secrets:


<code>

AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app

</code>


# AZURE-CICD-Deployment-with-Github-Actions

Save pass:

AAAAAAAAAAytiVnJ3h+CCCCCCCCf9q1vNwEi6+q+WGdd+BBBBBBBBB 

Run from terminal:

docker build -t chickenapp.azurecr.io/chicken:latest .

docker login chickenapp.azurecr.io

docker push chickenapp.azurecr.io/chicken:latest

Deployment Steps:

1. Build the Docker image of the Source Code
2. Push the Docker image to Container Registry
3. Launch the Web App Server in Azure
4. Pull the Docker image from the container registry to Web App server and run


