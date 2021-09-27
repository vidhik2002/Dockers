# Installation
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
