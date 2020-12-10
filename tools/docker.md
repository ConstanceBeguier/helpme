# Docker

## Install
@tags: docker install

```
# Install docker (Ubuntu)
$ sudo apt-get install docker.io
```


## Images management
@tags: docker images

```
# Search an image
$ docker search tensorflow

# Show all local images
$ docker search tensorflow

# Rename the image 9bf93bf90865 into test:v12 
$ docker tag 9bf93bf90865 test:v12

# Save a docker image into a tar file
$ docker save test:v12 test_v12.tar

# Load a tar file containing a docker image
$ docker load test_v12.tar

# Delete a docker image
$ docker rmi test:v12
$ docker rmi 9bf93bf90865
```

## Containers management
@tags: docker containers

```
# Launch a container in interactive mode
$ docker run -it tensorflow/tensorflow:latest /bin/bash
# This command has many arguments
# - [port forwarding] -p port_container:port_host
# - [mount a directory] -v path_host:path_container[:ro]
# - [container working directory] -w $PWD
# - [detach] -d
# - [delete the container at the end] --rm

# Launch a container with script argument
$ docker run -t --entrypoint path_script_in_container repository:tag script_args

# Show all containers
$ docker ps -a

# Stop a container
$ docker stop 9bf93bf90865
$ docker kill 9bf93bf90865

# Delete a container
$ docker rm 9bf93bf90865

# Save the container state into an image
$ docker commit 9bf93bf90865

# Delete all stopped containers
$ docker system prune
```

## Dockerfiles
@tags: docker dockerfiles build

```
# Dockerfile (example)
# Source image
FROM tensorflow/tensorflow:latest
# Install curl package
RUN apt-get update && apt-get install -y curl
# Create training directory
RUN mkdir training
# Update working directory
WORKDIR training
# Add config.sh file
ADD config.sh .
# Run config.sh file
RUN bash config.sh
# Define command to launch when starting the container
CMD /bin/bash
```

```
# Create a docker image from a dockerfile
$ docker build -t test_image .
```


