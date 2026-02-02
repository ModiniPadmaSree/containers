This document explains how to install Docker on cloud virtual machines across AWS EC2, Azure VM, and Google Cloud Compute Engine, followed by building and running a Docker container using a sample NGINX web server.  
Prerequisites:  
1. An instance in cloud platform(ubuntu)
2. SSH access to instance  
1. Docker installation  
- AWS: sudo apt update
sudo apt install -y ca-certificates curl gnupg lsb-release  
curl -fsSL https://get.docker.com | sudo bash  
sudo systemctl start docker  
sudo systemctl enable docker  
docker --version  
- Azure: sudo apt update  
sudo apt install -y curl  
curl -fsSL https://get.docker.com | sudo bash  
sudo systemctl start docker  
sudo systemctl enable docker  
docker --version  
- GCP: sudo apt update  
sudo apt install -y curl  
curl -fsSL https://get.docker.com | sudo bash  
sudo systemctl start docker  
sudo systemctl enable docker  
docker --version  
2. Create a file with name Dockerfile 
3. Create a index.html file 
4. Build and run the Docker image  
   docker build -t nginx-docker-app .
5. Run the container  
   docker run -d -p 80:80 --name nginx-container nginx-docker-app
6. Verify  
   docker ps
7. Access the application  
   http://ip_of_vm
8. If required cleanup - Stop and remove the containers  
   docker stop nginx-container  
   docker rm nginx-container
