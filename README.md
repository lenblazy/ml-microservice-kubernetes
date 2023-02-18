[![lenblazy](https://circleci.com/gh/lenblazy/ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/lenblazy/ml-microservice-kubernetes)

# ML-MicroService-Kubernetes

## Project Overview
This project leverages a Machine learning Microservice which uses `sklearn` model. This model has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. More information [here](https://www.kaggle.com/c/boston-housing). It uses Flask API to enable API calls to the service.

## Project Requirements
- Python 3.7
- Docker
- Kubernetes

## How to run
- Clone this Repo to your local machine.
- In your terminal, run ```make setup```. This will switch your python to a virtual environment called `.devops`.
- Install required python dependencies using ```make install```.
- Perform Link checks for both python and Docker code using ```make lint```. Note, you have to install `hadolint` to lint docker.
- Run the application using shell command ```./run_docker.sh```.
- In order to upload to docker hub, edit the `upload_docker.sh` file. Make a replacement to this line `dockerpath="<your_docker_username>/<your_desired_project_name>"`. After that, you should run `./upload_docker.sh`.
- You can also deploy to kubernetes by running this command ```./run_kubernetes.sh```
