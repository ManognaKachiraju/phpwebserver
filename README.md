# phpwebserver
Hosting a Python Web Server on Docker Hub
This repository contains the code and instructions to host a simple Python web server on Docker Hub and run it on an EC2 instance.
Steps:
1. Create a Basic Python Web Server:
  Create an index.php file and also
  Create a server.py file 
  Write a dockerfile for the same

2.  Create an EC2 instance :
    Create an Ec2 instance on AWS and connect with it and start installing docker in it and clone the repo using the follwing commands:

sudo apt update -y
git clone https://github.com/ManognaKachiraju/phpwebserver.git

sudo apt-get update
sudo apt-get install docker.io -y
sudo usermod -aG docker $USER  # Replace with your system's username, e.g., 'ubuntu'
newgrp docker
sudo chmod 777 /var/run/docker.sock

3. Dockerizing python web server
 Build,Run,Push
 
 docker build -t phpwebserver .
 docker run -d -p 8000:8000 phpwebserver
 docker push manokac55/phpwebserver  #only after logging into dockerhub and tagging the image

 Check if the page is running succesfully or not by using
 http://<your ec2 instance ip address>:8000





