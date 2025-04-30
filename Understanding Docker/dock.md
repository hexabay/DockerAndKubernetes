Docker requires Linux Kernel OS. Even if we create containers for windows or mac, a small linux instance will be created on top of which the image will be placed.


Docker Engine follows OCI standards - Open Container Initiatives

All tools follow OCI.
Images, registry, containers are built following the specifications of OCI.



> Three Ways to run Docker:
> 
> - Locally (Docker Desktop)
> - Server (Docker Engine, Kubernetes)
> - Paas (Fargate, Cloud Run by Amazon)


Understanding the components involved here

1. WSL 2:
     * Windows Subsystem for Linux 2
     * It provides the Linux kernel to run on Windows without the need for Virtual Machines like VMWare, etc.
     * It is not a Linux Distribution (distro)
     * A kernel is like the engine of a car. Kernel is responsible for providing memory management, processors, networking of Linux OS.
     * WSL on its own, is not functional.

2. Ubuntu:
   * Ubuntu is a Linux distribution (distro)
   * It provides lots of tools like package management, networks, file systems, user permissions, etc.
   * Ubuntu runs on top of WSL 2.
   * It is like the driver seat of a car that enables a user to make use of above functionalities to interact with the kernel present in WSL 2
   * Ubuntu has its own kernel. But it is used when Ubuntu is installed on its own computer. Since, in this case, windows is the primary OS, Ubuntu make use of the kernel provided by windows (Microsoft) - WSL 2.

3. Docker:
    * Docker is a platform for containerizing an application with the aim to make it run in any environment.
    * Its main concepts:  <u> Build, Ship, Run </u>
      * Build a Docker Image
      * Log it in the Docker Registry
      * Run the application anywhere using Docker Containers
    * Docker commands are run on Ubuntu 

> How are these three interconnected?  
> 
> An application is built and ready for deployment.  
> DNS - GoDaddy.com  
> Host - free VPS from Fly.io, Railway, Render, Heroku
> 
> Docker is used to containerize and run different servers on each. For example, npm on frontend and postgreSQL for database.
> 
> Docker, on top of Ubuntu, makes use of it's CLI and other tools to create and run containers on the kernel (present in WSL 2)
 





1. Docker Desktop download and install from:

https://docs.docker.com/desktop/setup/install/windows-install/


It will install with WSL 2: It is Windows Subsystem for Linux 2 that enable windows to run Linux OS without a virtual box.

Sign in to Docker

2. Ubuntu from Microsoft Store

Ubuntu is a distribution that will interact with Docker in Linux

Sign in to 
3. 