# Docker

Docker is a centralized platform for packaging, deploying, and running applications. Before Docker, many users face the problem that a particular code is running in the developer's system but not in the user's system. So, the main reason to develop docker is to help developers to develop applications easily, ship them into containers, and can be deployed anywhere.

Docker was firstly released in March 2013. It is used in the Deployment stage of the software development life cycle that's why it can efficiently resolve issues related to the application deployment.

<b>What is Docker?</b>

Docker is an open-source centralized platform designed to create, deploy, and run applications. Docker uses container on the host's operating system to run applications. It allows applications to use the same Linux kernel as a system on the host computer, rather than creating a whole virtual operating system. Containers ensure that our application works in any environment like development, test, or production.

Docker includes components such as Docker client, Docker server, Docker machine, Docker hub, Docker composes, etc.

<b>Docker Containers</b>

Docker containers are the lightweight alternatives of the virtual machine. It allows developers to package up the application with all its libraries and dependencies, and ship it as a single package. The advantage of using a docker container is that you don't need to allocate any RAM and disk space for the applications. It automatically generates storage and space according to the application requirement.

<b>Advantages of Docker</b>

There are the following advantages of Docker -

1. It runs the container in seconds instead of minutes.
2. It uses less memory.
3. It provides lightweight virtualization.
4. It does not a require full operating system to run applications.
5. It uses application dependencies to reduce the risk.
6. Docker allows you to use a remote repository to share your container with others.
7. It provides continuous deployment and testing environment.

<b>Disadvantages of Docker</b>

There are the following disadvantages of Docker -

1. It increases complexity due to an additional layer.
2. In Docker, it is difficult to manage large amount of containers.
3. Some features such as container self -registration, containers self-inspects, copying files form host to the container, and more are missing in the Docker.
4. Docker is not a good solution for applications that require rich graphical interface.
5. Docker provides cross-platform compatibility means if an application is designed to run in a Docker container on Windows, then it can't run on Linux or vice versa.

<b>Docker Features</b>

Although Docker provides lots of features, we are listing some major features which are given below.

1. Easy and Faster Configuration
2. Increase productivity
3. Application Isolation
4. Swarm
5. Routing Mesh
6. Services
7. Security Management
8. Easy and Faster Configuration
9. This is a key feature of docker that helps us to configure the system easily and faster.

We can deploy our code in less time and effort. As Docker can be used in a wide variety of environments, the requirements of the infrastructure are no longer linked with the environment of the application.

1. Increase productivity

By easing technical configuration and rapid deployment of application. No doubt it has increase productivity. Docker not only helps to execute the application in isolated environment but also it has reduced the resources.

2. Application Isolation

It provides containers that are used to run applications in isolation environment. Each container is independent to another and allows us to execute any kind of application.

3. Swarm

It is a clustering and scheduling tool for Docker containers. Swarm uses the Docker API as its front end, which helps us to use various tools to control it. It also helps us to control a cluster of Docker hosts as a single virtual host. It's a self-organizing group of engines that is used to enable pluggable backends.

4. Routing Mesh

It routes the incoming requests for published ports on available nodes to an active container. This feature enables the connection even if there is no task is running on the node.

5. Services

Services is a list of tasks that lets us specify the state of the container inside a cluster. Each task represents one instance of a container that should be running and Swarm schedules them across nodes.

6. Security Management

It allows us to save secrets into the swarm itself and then choose to give services access to certain secrets.

It includes some important commands to the engine like secret inspect, secret create etc.


<b>Docker Architecture</b>

Before learning the Docker architecture, first, you should know about the Docker Daemon.

<b>What is Docker daemon?</b>
Docker daemon runs on the host operating system. It is responsible for running containers to manage docker services. Docker daemon communicates with other daemons. It offers various Docker objects such as images, containers, networking, and storage.

<b>Docker architecture</b>

Docker follows Client-Server architecture, which includes the three main components that are Docker Client, Docker Host, and Docker Registry.

<b>Docker Architecture</b>

1. Docker Client

Docker client uses commands and REST APIs to communicate with the Docker Daemon (Server). When a client runs any docker command on the docker client terminal, the client terminal sends these docker commands to the Docker daemon. Docker daemon receives these commands from the docker client in the form of command and REST API's request.

Note: Docker Client has an ability to communicate with more than one docker daemon.
Docker Client uses Command Line Interface (CLI) to run the following commands -

<code>docker build</code>

<code>docker pull</code>

<code>docker run</code>

2. Docker Host

Docker Host is used to provide an environment to execute and run applications. It contains the docker daemon, images, containers, networks, and storage.

3. Docker Registry

Docker Registry manages and stores the Docker images.

There are two types of registries in the Docker -

1. Pubic Registry - Public Registry is also called as Docker hub.

2. Private Registry - It is used to share images within the enterprise.

<b>Docker Objects</b>

There are the following Docker Objects -

1. Docker Images

Docker images are the read-only binary templates used to create Docker Containers. It uses a private container registry to share container images within the enterprise and also uses public container registry to share container images within the whole world. Metadata is also used by docket images to describe the container's abilities.

2. Docker Containers

Containers are the structural units of Docker, which is used to hold the entire package that is needed to run the application. The advantage of containers is that it requires very less resources.

In other words, we can say that the image is a template, and the container is a copy of that template.

<b>Docker Architecture</b>

<b>Docker Networking</b>

Using Docker Networking, an isolated package can be communicated. Docker contains the following network drivers -

1. Bridge - Bridge is a default network driver for the container. It is used when multiple docker communicates with the same docker host.
2. Host - It is used when we don't need for network isolation between the container and the host.
3. None - It disables all the networking.
4. Overlay - Overlay offers Swarm services to communicate with each other. It enables containers to run on the different docker host.
5. Macvlan - Macvlan is used when we want to assign MAC addresses to the containers.

6. Docker Storage - Docker Storage is used to store data on the container. 

Docker offers the following options for the Storage -

1. Data Volume - Data Volume provides the ability to create persistence storage. It also allows us to name volumes, list volumes, and containers associates with the volumes.
2. Directory Mounts - It is one of the best options for docker storage. It mounts a host's directory into a container.
3. Storage Plugins - It provides an ability to connect to external storage platforms.


<b>Docker Container and Image</b>

Docker container is a running instance of an image. You can use Command Line Interface (CLI) commands to run, start, stop, move, or delete a container. You can also provide configuration for the network and environment variables. Docker container is an isolated and secure application platform, but it can share and access to resources running in a different host or container.

An image is a read-only template with instructions for creating a Docker container. A docker image is described in text file called a Dockerfile, which has a simple, well-defined syntax. An image does not have states and never changes. Docker Engine provides the core Docker technology that enables images and containers.

You can understand container and image with the help of the following command.

<code>$ docker run hello-world  </code>

The above command docker run hello-world has three parts.

1. docker: It is docker engine and used to run docker program. It tells to the operating system that you are running docker program.

2. run: This subcommand is used to create and run a docker container.

3. hello-world: It is a name of an image. You need to specify the name of an image which is to load into the container.

<b>Docker Useful Commands</b>

Docker is natively Linux based software so that it provides commands to interact and work in the client-server environment.

Here, we have listed some important and useful Docker commands.

Check Docker version

<code>$ docker version  </code>

It shows docker version for both client and server.

Build Docker Image from a Dockerfile

<code>$ docker build -t image-name docker-file-location  </code>

-t : it is used to tag Docker image with the provided name.

Run Docker Image

<code>$ docker run -d image-name  </code>

-d : It is used to create a daemon process.

Check available Docker images

<code>$ docker images  </code>

Check for latest running container

<code>$ docker ps -l  </code>

-l : it is used to show latest available container.

Check all running containers

<code>$ docker ps -a  </code>

-a : It is used to show all available containers.

Stop running container

<code>$ docker stop container_id  </code>

container_id : It is an Id assigned by the Docker to the container.

Delete an image

<code>$ docker rmi image-name  </code>

Delete all images

<code>$ docker rmi $(docker images -q)  </code>

Delete all images forcefully

<code>$ docker rmi -r $(docker images -q)  </code>

-r : It is used to delete image forcefully.

Delete all containers

<code>$ docker rm $(docker ps -a -q)  </code>

Enter into Docker container

<code>$ docker exec -it container-id bash  </code>


<b>Docker Compose</b>

It is a tool which is used to create and start Docker application by using a single command. We can use it to file to configure our application's services.

It is a great tool for development, testing, and staging environments.
It provides the following commands for managing the whole lifecycle of our application.

1. Start, stop and rebuild services
2. View the status of running services
3. Stream the log output of running services
4. Run a one-off command on a service

To implement compose, it consists the following steps.

1. Put Application environment variables inside the Dockerfile to access publicly.
2. Provide services name in the docker-compose.yml file so they can be run together in an isolated environment.
3. run docker-compose up and Compose will start and run your entire app.

 Build and Run Docker App with Compose(webapp folder):

<code>$ docker-compose up   </code>

<b>Docker vs. Kubernetes</b>

Today, both Docker and Kubernetes are leading container orchestration tools in the DevOps lifecycle. Docker uses a containerization platform for configuring, building, and distributing containers, while Kubernetes is an Ecosystem for managing a cluster of Docker containers.

1. What is Docker?

Docker provides a containerization platform which supports various operating systems such as Linux, Windows, and Mac. It allows us to easily build applications, package them with all required dependencies, and ship it to run on other machines. The advantage of using Docker is that it provides benefits for both developers as well as a system administrator. For develops it focuses on writhing the code without worrying about the system. For a system administrator, it provides flexibility to reduces the number of systems for testing the applications.

Docker includes various features such as easy and faster configuration, manages security, use Swarm, routing mesh, application isolation, and increase productivity.

2. What is Kubernetes?

Kubernetes (also known as k8s) is an open-source platform developed by Google. It offers powerful, useful, and scalable tools for managing, deploying complicated containerized applications. The advantage of using Kubernetes is that it provides the best solution for scaling up the containers.

Kubernetes includes various features such as runs everywhere, automated rollouts and rollback, storage orchestration, Batch execution, secret and configuration management, horizontal scaling, and offers additional services.
