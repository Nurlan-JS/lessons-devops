# Jenkins installation

## Introduction

This is official installation for Jenkins but let's go with Docker, then Jenkins

# Docker installation

Банальная установка Docker

## Add Docker's official GPG key:

```
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

## Add the repository to Apt sources:

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

## Official install of Docker engine and compoes

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Synchronize versions

```
docker --version
ls
cd Downloads
# download amd64.deb
sudo apt-get install ./docker-desktop-amd64.deb
```

## Check Docker's position

```
cd /opt/docker-desktop
ls
```

## Launch the Docker Desktop

Enjoy :smile: your DevOps with :whale: and Software Development journey with :student:

# Jenkins installation

## Introduction

This is official installation for Ubuntu Installation

## Pull Jenkins image from Docker hub

```bash
sudo docker pull jenkins/jenkins
sudo docker run -p 8080:8080 --name=jenkins-master -d jenkins/jenkins
```

Go to localhost
`http://localhost:8080/login?from=%2F`

## Let's work with installation

```bash
docker ps
NAMES
*31ab065e775b*   jenkins/jenkins   "/usr/bin/tini -- /u…"   6 minutes ago   Up 6 minutes   0.0.0.0:8080->8080/tcp, 50000/tcp   jenkins-master
```

take container id and put in following script
![alt text](./jenkins-images/Screenshot%20from%202024-11-20%2018-02-25.png "Title")

```bash
docker exec -it 31ab065e775b bash
cat /var/jenkins_home/secrets/initialAdminPassword
```

![alt text](./jenkins-images/Screenshot%20from%202024-11-20%2018-04-52.png "Title")

We will have `cat /var/jenkins_home/secrets/initialAdminPassword` answer and put it into Jenkins cloud.

## In process

Following installation

![alt text](./jenkins-images/Screenshot%20from%202024-11-20%2018-05-02.png "Title")

## Add admin and localhost

![alt text](./jenkins-images/Screenshot%20from%202024-11-20%2018-08-36.png "Title")

## Sucess

Jenkins is officially installed!

![alt text](./jenkins-images/Screenshot%20from%202024-11-20%2018-13-08.png "Title")
