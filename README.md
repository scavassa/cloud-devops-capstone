# cloud-devops-capstone

This is the Capstone Project for the Cloud DevOps Engineer Nanodegree by Udacity

## Files

  * .circleci/config.yml
  * app/
  * deployment-eks.yml
  * Dockerfile
  * infrastructure.yml

#### .circleci/config.yml
Config file including all necessary steps for project's CI/CD Pipeline using CircleCI

#### app/
This folder contains the chosen application to be deployed by this project, [Helios Election System](https://github.com/benadida/helios-server)

#### deployment-eks.yml
This is a YAML file containing the Kubernetes deployment and load balancer used to provision the application into AWS EKS

#### Dockerfile
File containing directives for the container

#### infrastructure.yml
CloudFormation YAML file that contains instructions to provide all the necessary infrastructure on AWS, including: VPC, RDS Intances, Subnets, Groups, LoadBalancers, Gateways, Workers, EKS Cluster and etc.

## Instructions

1. You must have an AWS account and [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) proper setup.
2. You must have an GitHub account where you should fork/copy this repo.
3. You must have a CircleCI account and [set up your project](https://circleci.com/docs/2.0/overview/) repo with your CircleCI account.
4. You must hava a DockerHub account to register your Docker Images.
5. Configure the necessary [environment variables](https://circleci.com/docs/2.0/env-vars/#environment-variable-usage-options):

**AWS_ACCESS_KEY_ID**

aws-cli access key

**AWS_SECRET_ACCESS_KEY**

aws-cli secret

**AWS_DEFAULT_REGION**

Your AWS defaul region

**DB_NAME**

Arbitrary database name that will be used to configure you Amazon RDS with PostgreSQL

**DB_USER**

Arbitrary name of the RDS database user

**DB_PASS**

Arbitrary password of the user that connects to the RDS database

**DOCKER_USER**

You DockerHub username

**DOCKER_PASS**

Your DockerHub password or Access Token

**STACK_NAME**

Arbitrary stack name that will be used into CloudFormation script