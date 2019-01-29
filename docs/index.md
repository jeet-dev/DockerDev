
## Docker DevOPS - Documentation 

## Docker pull - This is to pull an image from Docker Hub
```
Docker pull busybox 

```

## You can use the docker images command to see a list of all images on your system.

```
Docker images

```

## Docker run - This command will pull and run the container from the image pulled from Docker Hub Repo

```
Docker run busybox:1.30

Docker run -d busybox:1.30 # Run container in detached mode

Docker run -d -it  busybox:1.30 # Run the container in detached and interactive node

Docker exec -it <container id > # Open the interactive shell for the container
```

## Manage Running containers

```
docker ps -a

docker ps -aq # get the container id 

```
## Removing stopped containers

```
docker rm $(docker ps -a -q -f status=exited) # status = exited

docker container prune # remove al stopped containers

```

## Docker Port Mapping 

```

docker run -it -d -p 9000:8080 tomcat:8.0

```
## Docker Logs

```
docker logs <container id>

```

## Docker Image Layers 

```

Docker history < image > # this command will show the layers of images on the base image.

```
## Docker File 

```

A Docker file is a text docuemnt that contains all the instructions users provided to assemble an image. 


FROM debian:7.11
RUN apt-get update 
RUN apt-get install -y git 
RUN apt-get install -y vim


```
## Docker Build 

```
Docker Build command will build the docker file instructions and create an image with the tag provided.

docker build -t jeetdev0ps/debian:1.0 .


```

