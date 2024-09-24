
# Docker Tutorial


- Docker is a centralized platform for packaging, deploying, and running applications. Before Docker, many users face the problem that a particular code is running in the developer's system but not in the user's system. So, the main reason to develop docker is to help developers to develop applications easily, ship them into containers, and can be deployed anywhere.

- Docker was firstly released in **March 2013**. It is used in the Deployment stage of the software development life cycle that's why it can efficiently resolve issues related to the application deployment.


## Verify Docker Engine

```bash
docker --version
```

## Docker Engine Work

```bash
docker info
```

## Docker image How to download

```bash
docker pull image--name
```

## Docker image How to Show

```bash
docker images
```

## Docker run

```bash
docker run image--name
```

## How to running Containers See comment

```bash
docker ps
```

## How to All Containers See comment

```bash
docker ps -a
```

## Docker file in projects
```bash
#use a base image
FROM alpine:lateast

#run a comment
CMD ["echo","Hello,Docker"]
```


## Build Docker

```bash
docker build -t my-simple-image .
```

## Docker node pull

```bash
docker pull node
```

## Docker node run 

```bash
docker run node
```


## Docker container start 

```bash
docker start container_name
```

## Already Docker container start  not stoped comment

```bash
docker exec -it container_name node
```


## (or) Already Docker container start  not stoped comment Path way

```bash
docker exec -it container_name /bin/bash

cd /usr/localbin/bin

node
```

## Containers Name create

```bash
docker run --name node_imagename node_containername
```

## Containers ReName create

```bash
docker rename node_imagename newnode_imagename 
```


## Containers not running containers all deleted

```bash
docker container prune
```

## Copy file to container

- my_sample.txt file to create a file
```bash
docker pull alpine

docker run -it --name my_alpina_container

ls


```  
not stoping this comment new open terminal

current working txt file path open terminal

```bash
docker cp .\my_example.txt  container_name:/example.txt
docker cp .\my_example.txt  container_name:/var/example.txt


```
copy to the file conatiner name var path inside 


## Read file

```bash
cat example.txt
```


## Copy file from container

```bash
docker cp container__name:/file_name.txt ./exmple_copy.txt
```

## publishing Docker images


- Dockerfile create a file name

```bash 
FROM alpine:lateast
CMD echo "Hello,Docker"

```

open terminal 

```bash
docker build -t image_name . 
```

The next step to a DockerHub to publish

- Repositories
- create Repositories
- repo name & descrption
- public
- create


```bash 
docker login




docker tag my-simple-image  selvalr/my-simple-image-repo:latest


docker push selvalr/my-simple-image-repo:latest
```



## pulling & Run DockerHub images

first delete the docker image to a your already pushing a data in docler container

```bash

docker pull selvalr/my-simple-image-repo:latest


docker run -it selvalr/my-simple-image-repo
```
