## Docker Terminology

### What is Docker?

> Docker is a platform or ecosystem around creating and running containers. It contains of the Docker - client, server, hub etc.

### Why use Docker?

> Docker makes it really easy to install and run software without worrying about the setup and dependencies.
> Developing apps today requires so much more than writing code. Multiple languages, frameworks, architectures, and discontinuous interfaces between tools for each lifecycle stage creates enormous complexity. Docker simplifies and accelerates your workflow, while giving developers the freedom to innovate with their choice of tools, application stacks, and deployment environments for each project.

### Container Image

A package with all the dependencies and information needed to create a container. An image includes all the dependencies (such as frameworks) plus deployment and execution configuration to be used by a container runtime. Usually, an image derives from multiple base images that are layers stacked on top of each other to form the container's filesystem. An image is immutable once it has been created.

### Build

The action of building a container image based on the information and context provided by its Dockerfile, plus additional files in the folder where the image is built. You can build images with the following Docker command : <br>
```
docker build
```

### Container

An instance of a Docker image. A container represents the execution of a single application, process, or service. It consists of the contents of a Docker image, an execution environment, and a standard set of instructions. When scaling a service, you create multiple instances of a container from the same image. Or a batch job can create multiple containers from the same image, passing different parameters to each instance.

### Docker run in detail

Creating and running a Container from the image

```
$ docker run image-name
```

Whenever we execute this command, it first **creates a writeable container layer over the specified image**, and then **starts it using the specified command**. That is, docker run is equivalent to the API **/containers/create** then **/containers/(id)/start**. A stopped container can be restarted with all its previous changes intact using **docker start**. 

To List all the containers created

See ```docker ps -a``` to view a list of all containers.
