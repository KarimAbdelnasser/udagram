# Introduction
This documentation outlines the steps involved in the CircleCI pipeline process for a project using CircleCI version 2.1. The pipeline is divided into two stages: building and deploying.

## Building Stage
The building stage is responsible for installing dependencies, checking out code, and building the frontend and backend components of the project.

-The base image "cimg/node:14.15" is used for the build job.

-The AWS CLI and Elastic Beanstalk orbs are included in the pipeline for setup.

-Node and its dependencies are installed using the node/install step.

-The code is checked out using the checkout step.

-The frontend dependencies are installed using this command.
```bash
npm run frontend:install
```
-The backend API dependencies are installed using this command.
```bash
npm run api:install
```
-The frontend is linted using this command.
```bash
npm run frontend:lint
```
-The frontend app is built using this command.
```bash
npm run frontend:build
```
-The backend API is built using this command.
```bash
npm run api:build
```
## Deploying Stage
The deploying stage is responsible for deploying the built components to AWS Elastic Beanstalk.

-The base image "cimg/base:stable" is used for the deploy job.

-The AWS CLI and Elastic Beanstalk orbs are included in the pipeline for setup.

-Node and its dependencies are installed using the node/install step.

-The code is checked out using the checkout step.

-The AWS CLI is configured using environment variables for access key and secret key.

-The deployment is triggered using this command.
```bash
npm run deploy
```
## Workflows
The CircleCI pipeline is defined using the workflows section. The workflow in this configuration file consists of the following steps:

-The build job is run first.

-The deploy job is run after the build job and manual approval.