[Go to README.md](../README.md)
# Installing docker and docker-compose
## Installing docker option 1

This way is also described in [docker help pages](https://docs.docker.com/engine/install/ubuntu/)

### Set-up docker repositories
Install packages needed Docker to run on your system:
```
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
```
Add docker's GPG key

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
Finally, add Docker's repository to your system:
```
sudo add-apt-repository \
   "deb [arch=arm64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
``` 
### Install Docker engine:
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```


## Installing docker option 2
Get the installation script from Docker site:
```
curl -fsSL https://get.docker.com -o get-docker.sh
```
Check the content of the sccript and then if everything is Okay for you, run it:
```
sudo sh get-docker.sh
```
That will install Docker on your system


## Check Docker has been installed and is able to work
```
docker version
sudo docker run hello-world
```
### [Optional] Docker post-install
To allow Docker run without ```sudo```, i.e. as non-root user run the following: 
```
sudo groupadd docker
sudo usermod -aG docker ${USER}
newgrp docker
```
## Installing Docker-compose

### Install dependencies
```
sudo apt-get install libffi-dev libssl-dev
sudo apt install python3-dev
sudo apt-get install -y python3 python3-pip
```
### install docker-compose via pip3
```
sudo pip3 install docker-compose
```
Check if docker-compose is installed correctly:

```
docker-compose --version
```
Command should return the version of docker-compose.

[Go to README.md](../README.md)