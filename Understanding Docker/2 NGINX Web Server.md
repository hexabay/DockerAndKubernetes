# NGINX Web Server

Image: source code, binaries, libraries of an application

Container: an instance of the image running as a process; can have as many containers of an image

Registry: place where we get images from, like NGINX web server image (for docker, docker hub is the default registry)


Commands

### Run a container instance of nginx image

1. To download an image and publish it in a container:  

    `docker container run --publish 80:80 -d --name webhost nginx`

   - starts new container
   - `--publish` will open a port 80 in the host and route all the traffic in the web to port 80 of the container running nginx
   - `-detach | -d ` will tell docker to run in the background

    
2. To view containers and images
    
    `docker container ls` : to list all containers running
    
    `docker container ls -a` : to list all containers running or otherwise 

   `docker image ls` : to list all images available

    `ctrl` + `c` will only stop running the container. It wont delete it.

   `docker ps` shorthand linux command- same 


3. To stop a running container
    
    `docker container stop ___` 
    
    - Container ID - this command will stop that particular container.
    - Container id and name must be unique


4. To check container logs:

    `docker container logs <container name>`


5. To remove containers:

    `docker container rm <container id>`  
    `docker container rm -f <container id>` to force delete a running container


6. To view processess running in a container

   `docker top mongo`


7. Delete all exited containers at once

   `docker rm $(docker ps --filter status=exited -q)`

   - ps means process status. It will list all containers running. `-a` will list all.
   - filtering based on status as exited
   - -q | --quiet is to run without output. When commands are chained, -q is used and based on its results, exterior command works.