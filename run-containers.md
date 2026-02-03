This document explains how to create and run Docker containers using the Docker Command-Line Interface (CLI) on cloud platforms including AWS EC2, Virtual Machines, and Google Cloud Compute Engine. Since Docker works consistently across environments, the same commands apply to all platforms once Docker is installed.  
Prerequisites:  
1. Linux VM (Ubuntu preferred) on AWS, Azure, or GCP
2. Docker installed and running
3. SSH access with sudo privileges  
  
Commands using the Docker CLI  
1. Verify docker installation: docker --version  
   Check Docker status: sudo systemctl status docker
2. Pull images from docker registry: docker pull image_name  
   For nginx: docker pull nginx  
   For ubuntu: docker pull ubuntu:latest
3. Verify downloaded images: docker images  
4. Running containers: docker run [options] images [command] [args]  
   Run an nginx container: docker run -d -p 80:80 --name nginx-container nginx  
   Run an ubuntu container(Interactive mode): docker run -it --name ubuntu-container ubuntu /bin/bash  
   -d: running container in detached mode(background)  
   --name: assign name to the container  
   -p: map container port to host port  
5. Check running containers: docker ps 
6. Check all the containers (incl. stopped): docker ps -a
7. Verify container logs: docker logs nginx-container
8. Stopping container:  
   docker stop nginx-container
9. Restart container: docker start nginx-container
10. Removing container:  
   docker stop nginx-container  
   docker rm nginx-container  
  
The Docker CLI commands listed above work identically on:  
AWS EC2  
Azure Virtual Machines  
Google Cloud Compute Engine


