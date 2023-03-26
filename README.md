
<p align="center">
<img src="https://user-images.githubusercontent.com/76872523/227756067-5aecd356-39bb-4309-9d20-8ffc26e162e0.png">
</p>

#####  A collection of resources that helped me understand Dockers!
Docker is a software platform that allows you to build, test, and deploy applications quickly.
## Installation
Make sure your WSL is upgraded to version 2.


#### To check if its upgraded 
Open PowerShell as administrator
```sh
wsl -l -v
```
Follow the link to upgrade WSL
https://winaero.com/install-windows-subsystem-for-linux-2-in-windows-10/


#### Docker Setup
To uninstall older version
```sh
sudo apt-get remove docker docker-engine docker.io containerd runc
```
Run the convenient script
```sh
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```
To start docker daemon
```sh
sudo dockerd
```
To check the current version of docker
```sh
docker version
```
##### Commands
To pull an image
```sh
docker pull hello-world
```
To check the list of containers running 
```sh
docker ps
```
To check the list of all containers 
```sh
docker ps -a
```
To containerize an image
```sh
docker run redis
```
To remove an image
```sh
docker rmi -f redis
```
To pull a specfic image version from dockerhub and containerize it
```sh
docker run redis:4.0
```
To run docker in detached mode
```sh
docker run -d redis:4.0
```
We can use this id to start and stop a docker
```sh
docker start <id>
docker stop <id>
```
Port Binding
```sh 
docker run -p6000:6379 redis
```
Debugging container
```sh 
docker exec -it <id> /bin/bash 
```
Networking
```sh
docker network ls
```
To delete an image, we need to stop the container and remove its container first
```
docker ps
docker stop <Container_Id>
docker rm <Container_Id>
docker image rm <Image_Id>
```

