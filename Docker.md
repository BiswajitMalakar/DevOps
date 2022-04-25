# Docker

[Click here](https://docs.docker.com/get-started/overview/) to get Docker official doc.

Before jump into Docker we have to have little knowledge about [Containers](https://www.ibm.com/cloud/learn/containers) & [Virtual Machines](https://www.ibm.com/in-en/cloud/learn/virtual-machines).

---

What if I told you to share your app (web app) to 100 people ?
They must install all of the frameworks, libraries, languages in order to run your application. This might take some time and effort to do all those things manually.
Question is there has any way to do all those things automatically ? 
The answer is Yes. We can use the concept of containerization. Docker and other tools helps to do that.

# What is Docker ?

Docker helps you to create container to developing, shipping, and running applications so that you can deliver your apllication quickly and easily.
Docker lets you create Dockerfile that may contain your application and all the dependencies needs to run your application. Using that Dockerfile you can create Dockerimage and this lets you create containers. And all of these things ensure that your application will run on all environments.

# What is Container ?

Think of it like a box or a folder that can store your application source code, libraries and all the dependencies that are required to run your application.

# What are Images ?

Images are the blue print of Containers, it lets you decide the structure of the container and what should be inside of the container. Using an Image you can create a container that you can run on your machine.
If you want to share a container with your friend in that case you will not share the actual container but the image.
In short Image is the blue print and Container is the actual product.

# What is Dockerfile ?

If you want to create an Image for yourself you will not create an image but a Dockerfile. It is a file that you will create on your machine to build an Image to share.

**In short a Dockerfile helps you create an Image and an Image helps you to create a Container**

# Architecture of Docker

![Hello Docker](E:\90DaysOfDevops\assets\images\architecture.png)
Docker follows the client-server architecture. Here you as a client request for somthing using Docker CLI and Docker will response back to you.

# Basic Docker Commands

` docker run image-name `
` docker pull image-name `
` docker images `
` docker run -it image-name `
` docker ps `
` docker container ls `
` docker exec -it container-id bash `
` docker stop container-id `
` docker ps -a `
` docker rm container-id `
` docker inspect container-id/container-name `
` docker logs container-id `
` docker container prune -f `
` docker run alpine ping url/ip `
` docker run ubuntu echo Hello `
` docker logs --since argument container-id `
` docker rmi image-id/image-name `
` docker start container-id `
` docker commit -m "message" container-id new-container-name:new-container-version `
` docker run -it new-container-name:new-container-version `
` docker images -q `
` docker rmi $(docker images -q) -f `

` 
FROM image-name
MAINTAINER Biswajit Malakar <mebiswajitmalakar@gmail.com>
RUN command
CMD ["command-name", "argument-that-the-command-is-taking"]
`

` docker login `
' docker build -t new-image-name path-to-that-image `

` Docker-client ---> Docker Daemon ----> containerd ----> shim ---> runc ---> container `![](C:\Users\mebis\AppData\Roaming\marktext\images\2022-04-22-20-04-26-image.png)