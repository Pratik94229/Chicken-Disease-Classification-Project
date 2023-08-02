# Chicken Coccidiosis Classification

This project aims to classify chicken fecal samples into two categories: diseased (Coccidiosis) and healthy. The classification is based on analyzing images of the fecal samples using computer vision techniques.

## Project Structure

The project follows a modular structure, consisting of several stages and pipelines which includes :-

1. `stage_01_data_ingestion.py`: This stage is responsible for data ingestion. It includes functions for downloading, extracting, and preprocessing the dataset.
2. `stage_02_prepare_base_model.py`: In this stage, the base model for the classification task is prepared. It involves loading a pre-trained model, modifying it if necessary, and preparing it for training.
3. `stage_03_training.py`: The training stage is responsible for training the model using the prepared dataset. It includes functions for data augmentation, model training, and saving the trained model.
4. `stage_04_evaluation.py`: This stage focuses on evaluating the performance of the trained model. It includes functions for loading the trained model, performing inference on test data, and calculating evaluation metrics.

## Dependencies

To run this project, you need the following dependencies:

- Python (version 3.8 or above)
- TensorFlow 
- Flask 
- DVC 

Make sure you have installed the required dependencies before running the project.


## Workflows
* Update config.yaml
* Update secrets.yaml [Optional]
* Update params.yaml
* Update the entity
* Update the configuration manager in src config
* Update the components
* Update the pipeline
* Update the main.py
* Update the dvc.yaml

## Usage

1. Clone the repository:

```bash
git clone https://github.com/Pratik94229/Chicken-Disease-Classification-Project

```
```
cd Chicken-Disease-Classification-Project
```

2. Create a conda environment after opening the repository
```
conda create -p venv python==3.8 
conda activate venv/

```

3. Install the dependencies:

```bash
pip install -r requirements.txt
```


4. Finally run the following command

```
python app.py

```

5. Open Terminal

### DVC cmd
```
dvc init
dvc repro

```
6. For visualizing pipeline
```
dvc dag

```

7. Flask App:

To create a front-end interface for the application, run the Flask app:

```bash
python app.py
```

8. Access the app:

Open your browser and go to 

`http://localhost:5000` to access the application.


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

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

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 738400679807.dkr.ecr.ap-south-1.amazonaws.com/chicken

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  738400679807.dkr.ecr.ap-south-1.amazonaws.com/chicken

    ECR_REPOSITORY_NAME = simple-app




# AZURE-CICD-Deployment-with-Github-Actions

## Save pass:

s3cEZKH5yytiVnJ3h+eI3qhhzf9q1vNwEi6+q+WGdd+ACRCZ7JD6


## Run from terminal:

docker build -t chickenapp.azurecr.io/chicken:latest .

docker login chickenapp.azurecr.io

docker push chickenapp.azurecr.io/chicken:latest


## Deployment Steps:

1. Build the Docker image of the Source Code
2. Push the Docker image to Container Registry
3. Launch the Web App Server in Azure 
4. Pull the Docker image from the container registry to Web App server and run 



## About MLflow & DVC

MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & taging your model


DVC 

 - Its very lite weight for POC only
 - lite weight expriements tracker
 - It can perform Orchestration (Creating Pipelines)

## Conclusion

This project demonstrates the classification of chicken fecal samples as diseased or healthy using computer vision techniques. The modular structure and the use of pipelines make it easy to follow and reproduce the workflow. The Flask app provides a user-friendly interface for interacting with the classification model.

For more details, refer to the individual implementation files and comments within the code.
