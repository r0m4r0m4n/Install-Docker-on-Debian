# How to Install-Docker-on-Debian

## UNINSTALL OLD VERSIONS:

`sudo apt-get remove docker docker-engine docker.io containerd runc`

## SET UP THE REPOSITORY:

Update the apt package index and install packages to allow apt to use a repository over HTTPS:
sudo apt-get update
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```
Add Docker’s official GPG key:
```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
```
Use the following command to set up the stable repository:

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
```
## INSTALL DOCKER ENGINE:
Update the apt package index, and install the latest version of Docker Engine and containerd, or go to the next step to install a specific version:
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
Verify that Docker Engine is installed correctly by running the hello-world image.

`sudo docker run hello-world`
