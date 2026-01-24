# docker
#What is Docker?

---
Docker is an OS‑level virtualization (or containerization) platform, which allows applications to share the host OS kernel instead of running a separate guest OS like in traditional virtualization. This design makes Docker containers lightweight, fast, and portable, while keeping them isolated from one another.

Written in the Go programming language.
Supports Windows, macOS, and Linux installations (Docker Engine runs natively on Linux).
Solves the “works on my machine” problem by ensuring code runs identically across environments.
Unlike VMware (hardware‑level virtualization), Docker operates at the OS level.

#Before Docker:
Deploying applications across environments was often difficult, dependencies, configs, and OS variations caused “works here but not there” headaches.
<img width="1000" height="500" alt="dockervsvm" src="https://github.com/user-attachments/assets/339d4549-fc31-4d4e-b992-bad63f1135d8" />
<img width="1000" height="500" alt="dockervsvm" src="https://github.com/user-attachments/assets/f7de98e3-6f3e-470e-b36a-d715d523ef34" />

---
#Docker’s Solution:

---
Standardizes the runtime environment by bundling everything (app + dependencies) into containers.

Portability: Runs anywhere in local machine, cloud, on‑prem servers.
Consistency: Same behavior in development, testing, and production.
Lightweight: No full OS per app; containers share the host kernel.
Scalability: Ideal for microservices and orchestrators like Kubernetes and Docker Swarm.
Efficiency: Starts in seconds, uses fewer system resources.
Understanding Docker's core concepts is essential, but practical experience is what truly sets you apart. Platforms like Hostinger make it easy to deploy Docker containers, allowing you to focus on developing and testing your applications. Hostinger's scalable infrastructure provides an ideal environment for learning and experimenting with Docker in a real-world setting. Their seamless integrationwith Docker containers ensures that whether you're running simple apps or complex multi-container setups, you can deploy with ease.
 

---
#Components of Docker

---
The following are the some of the key components of Docker:

Docker Engine: Docker Engine has a core part docker daemon , that handles the creation and management of containers.
Docker Image: Docker Image is a read-only template that is used for creating containers, containing the application code and dependencies.
Docker Hub: It is a cloud based repository that is used for finding and sharing the container images.
Dockerfile: It is a file that describes the steps to create an image quickly.
Docker Registry : It is a storage distribution system for docker images, where you can store the images in both public and private modes.

---

#Docker Engine

---
The Docker Engine is the core component that enables Docker to run containers on a system. It follows a client-server architecture and is responsible for building, running, and managing Docker containers.

The Docker Engine Daemon (dockerd) runs in the background, listening to API requests and managing objects like images, containers, networks, and volumes.
The Docker Client (docker CLI) communicates with the daemon using a REST API. It provides the execution environment where Docker Images are instantiated into live containers.
Without the Docker Engine, Docker images cannot be built or containers executed.

The Client sends Docker commands (docker build, docker run, etc.).
The Daemon receives these commands and performs container operations.
The REST API is the interface enabling this communication.
In short, the Docker Engine is the runtime that makes containerization possible by connecting the Docker client with the daemon to build and manage containers efficiently.

---

#Dockerfile

---

The Dockerfile uses DSL (Domain Specific Language) and contains instructions for generating a Docker image. Dockerfile will define the processes to quickly produce an image. While creating your application, you should create a Dockerfile in order since the Docker daemon runs all of the instructions from top to bottom.

The Dockerfile is the source code of the image.

(The Docker daemon, often referred to simply as "Docker," is a background service that manages Docker containers on a system.)

It is a text document that contains necessary commands which on execution help assemble a Docker Image.
Docker image is created using a Dockerfile.

<img width="1000" height="362" alt="dockerfile-2" src="https://github.com/user-attachments/assets/ac8720a3-3a42-4020-b160-697f9c3789e6" />

---

#Docker Architecture and Working

---
Docker makes use of a client-server architecture. The Docker client talks with the docker daemon which helps in building, running, and distributing the docker containers. The Docker client runs with the daemon on the same system or we can connect the Docker client with the Docker daemon remotely. With the help of REST API over a UNIX socket or a network, the docker client and daemon interact with each other. To know more about working of docker refer to the Architecture of Docker .

<img width="1000" height="382" alt="Architecture-of-Docker" src="https://github.com/user-attachments/assets/de95aed9-9403-4fff-a039-0e9e52a06552" />

Docker CLI
Command-line interface to interact with Docker
Common commands: docker run, docker build, docker pull
Docker Rest API
HTTP API used by the CLI and other tools
Facilitates communication with the Docker daemon
Docker Daemon
Handles images, containers, networks, and volume
Core service that manages Docker objects
High-Level Runtime
Manages container lifecycle operations
Tasks include create, start, stop, and delete containers

---
#Docker Image

A Docker Image is a file made up of multiple layers that contains the instructions to build and run a Docker container. t acts as an executable package that includes everything needed to run an application — code, runtime, libraries, environment variables, and configurations.

How it Works:

The image defines how a container should be created.
Specifies which software components will run and how they are configured.
Once an image is run, it becomes a Docker Container.
Relation to Containers:

Docker Image → Blueprint (static, read-only).
Docker Container → Running instance of that image (dynamic, executable)

#Docker Container

A Docker Container is a lightweight, runnable instance of a Docker Image. It packages the application code together with all its dependencies and runs it in an isolated environment. Containers allow applications to run quickly and consistently across different environments — whether on a developer’s laptop, test servers, or production.

A container is created when a Docker Image is executed.
It runs as an isolated process on the host machine but shares the host’s operating system kernel.
Multiple containers can run on the same system without interfering with each other.
For eg - Suppose there is an image of Ubuntu OS with NGINX SERVER when this image is run with the docker run command, then a container will be created and NGINX SERVER will be running on Ubuntu OS. 

Relation to Images:

Docker Image = Blueprint (static, read-only).
Docker Container = Live instance of that blueprint (dynamic, executable)

