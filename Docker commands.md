Docker Commands

Installing Docker on AWS Linux EC2 Instance 

sudo su -

yum update

yum install docker 

docker info

usermod -aG docker root

service start docker 

docker info

docker create --name <container name> <image name> Ex: docker create --name demo ubuntu

docker start <container name> Ex: docker start demo

Docker run command is combination of both create and start

docker run -it --name <container name> <image name> 

Ex: docker run -it --name demo1 ubuntu(interactive mode)

docker run -dt --name <container name> <image name> 

Ex: docker run -it --name demo1 ubuntu ( Detached mode)

docker pause <container name>

docker unpause <container name>

docker stop <container name>

To stop all the running containers

docker stop $(docker container ls –aq)

docker rm <container name>

To remove all the non running containers

docker rm $(docker ps -aq)

Can kill running containers

docker kill <container name>
