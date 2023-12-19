# docker_flask_homework


## What is Docker 

Docker is an OS-level virtualization where isolated pieces of software are placed into containers in order to solve the problem of bugs being generated in different environments when deploying an application. 


## Part 1: 

1. Create repository for this assignment and cloned it to my google shell terminal 
2. Create the necessary folders in the folder ‘Part1’ which are necessary to dockerize my flask application 
3. This folder contains a flask application under file app.py and a requirements.txt file 
4. Create a Dockerfile for the flask application created



### DOCKER CODE 

Dockerfile Breakdown: 

Command ‘FROM’ selects the base package of software used for this application, otherwise known as a docker image. This base image is used to create a docker container image. 

Command ‘WORKDIR/ app’ sets the working directory inside the container to /app
All file commands will be run within this directory 

Command ‘COPY ./app’ duplicates the original directory files and copies it to the new location of ./app located in the container

Command ‘RUN pip install -r requirements.txt’ install the dependencies within this file 

Command ‘EXPOSE 5000’ creates the container on the given port 

Command ‘CMD [“python”, “app,py”] runs the app.py file 



### Running Docker 

### Name Application 

```Docker build command: docker build -y (application name) ```

### Run Docker 

```Docker run command: docker run -d -p 8000:5000 (application name)```

### View Docker Images 

```Docker images```

### View Active Docker Images

```Docker ps```

### Stop Docker 

```Docker stop [CONTAINER ID]```



## Part 2: Dockerizing Two Flask Applications 

1. Create two different flask application which are supplemented by requirements.txt and docker files
2. Create a docker-compose.yaml file which contains the two containers flask app 1 and flask app 2 which were just created 
