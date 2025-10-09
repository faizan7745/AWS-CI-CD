# AWS-CI-CD
🚀 A  Flask-based web application deployed using AWS Managed DevOps Services — GitHub, CodePipeline, CodeBuild, and CodeDeploy. This project demonstrates a complete CI/CD automation workflow on AWS for a Python Flask app running on EC2.

This repository contains a Dockerized Python Flask app and the required deployment files (e.g., appspec.yaml, deployment scripts, buildspec.yml) to automate build and deploy using AWS Code* services. The pipeline builds the Docker image (CodeBuild), pushes to Docker Hub, then CodeDeploy pulls the artifact/scripts and runs startcontainer.sh on EC2 instances.

Prerequisites

• AWS account with permissions to create IAM roles, CodeBuild, CodePipeline, CodeDeploy, EC2.

• GitHub repository with this code.

• Docker Hub account (or another registry).

• Replace placeholders in commands below: <AWS_REGION>, <GITHUB_REPO_URL>, <DOCKERHUB_USERNAME>, <IMAGE_NAME>, <IMAGE_TAG>, <EC2_INSTANCE_ID>, <SERVICE_ROLE_NAME>, <EC2_INSTANCE_PROFILE_NAME>.and also in AWS SSM(parametre store).

• AWS CLI installed (optional, for CLI steps).

STEPS:-
1] git clone https://github.com/faizan7745/AWS-CI-CD.git
2] cd AWS-CI-CD
3] Prepare IAM Users and Roles.:- 
            Attach Required policies like CodeBuild / CodePipeline / CodeDeploy / EC2 acess and so on.
4] Make required changes in Build spec — buildspec.yml (according to your need).
5] Add parameter in AWS SSM parameter store.
6] Setup CodeBuild for this repo. and check build's sucsses.
7] Setup Codepipeline for this codebuild.
8] Launch EC2 instance add Tag for that,install Docker,and Codedeploy Agent on it.
9] Setup Codedeploy for streamline deployment or rollout process on EC2 instance and acess webpage....
