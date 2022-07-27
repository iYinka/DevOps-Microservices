<include a CircleCI status badge, here>
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/iYinka/DevOps-Microservices/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/iYinka/DevOps-Microservices/tree/master)

## Project Overview

This project is inspired to create a model that predicts house prices in Boston. To acheive this, Machine Learning is employed using Microservice API which is built on Scikit-Learn.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:

-   Test your project code using linting
-   Complete a Dockerfile to containerize this application
-   Deploy your containerized application using Docker and make a prediction
-   Improve the log statements in the source code for this application
-   Configure Kubernetes and create a Kubernetes cluster
-   Deploy a container using Kubernetes and make a prediction
-   Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

-   Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv.

```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host.
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```

-   Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone: `python app.py`
2. Run in Docker: `./run_docker.sh`
3. Run in Kubernetes: `./run_kubernetes.sh`

### Kubernetes Steps

-   Setup and Configure Docker locally
-   Setup and Configure Kubernetes locally
-   Create Flask app in Container
-   Run via kubectl: `kubectl run ml-project --image=$dockerpath`

FILE DIRECTORIES
File/Directory Description
- Circleci -> Contains config.yml file
- Model Data -> Shows house prices in the Boston
- Output_files -> Contains docker and kubernetes log outputs
- app.py -> REST endpoint in flask containing routes to fetch house prices in boston
- Dockerfile -> Docker creation files with dependencies
- make_predictions.sh -> Script to log output predictions from the REST api end point
- Makefile -> Install project dependcies and lint
- requirements.txt -> Dependencies for the ml-project
- upload_docker.sh -> Shell script to upload locally built image to docker hub
- run_docker.sh -> Shell script to build the docker file
- run_kuberbetes.sh -> Shell script to run and start up docker image in kubernetes

#Cheers!
