# Docker Image

> ## Issue
> 
>       docker container run --publish 80:80 nginx
> 
> If image is unavailable locally, Ubuntu is unable to download the image automattically from Docker Hub.
> 
> This issue might get resolved once the DNS issue is resolved
> 
> Some proxy or firewall is blocking ubuntu/docker from accessing internet on its own.
> 
> 

### Work-around

- Open Docker Desktop
- Navigate to Docker Hub
- Search the image and pull it. This will make the image local.
- Now execute the previous command, it will work.

