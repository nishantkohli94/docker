Assignment 1 Docker

Use official shell script to install and configure Docker on your control machine.

my script didnt worked 

sudo yum -y install docker

Start Docker service and check status of the same.

sudo systemctl start docker
sudo systemctl status docker

Enable Docker service to start at every machine reboot.
sudo systemctl status docker

![](https://github.com/nishantkohli94/docker/blob/master/images/Capture_docker_running.PNG)

Display Docker version.

docker version

Configure non root user to run docker commands without sudo.
groupadd dockers
usermod -aG dockers docker

Display System information using Docker.
sudo docker system info

Check whether you can access/download images from DockerHub or not.

docker run hello-world

docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
9db2ca6ccae0: Pull complete
Digest: sha256:4b8ff392a12ed9ea17784bd3c9a8b1fa3299cac44aca35a85c90c5e3c7afacdc
Status: Downloaded newer image for hello-world:latest

docker ps -a
CONTAINER ID        IMAGE               COMMAND              CREATED             STATUS                         PORTS               NAMES
94c01e8cbce5        hello-world         "/hello"             20 seconds ago      Exited (0) 20 seconds ago                          determined_ritchie








