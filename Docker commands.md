Docker Commands

Installing Docker on AWS Linux EC2 Instance 

sudo su -

yum update

yum install docker 

docker info

usermod -aG docker root

service docker start 

docker info

docker create --name <container name> <image name> Ex: docker create --name demo ubuntu

docker start <container name> Ex: docker start demo

Docker run command is combination of both create and start

docker run -it --name <container name> <image name> 

Ex: docker run -it --name demo1 ubuntu bash (interactive mode)

docker run -dt --name <container name> <image name> 

Ex: docker run -dt --name demo2 ubuntu bash ( Detached mode)

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

To check docker container details 
go to /var/lib/docker/containers it has all the containers listed 

ps fxa | grep docker -A 3

docker attach <container-ID> (not harm to primary process)

docker exec -it <container-ID> bash (this starts secondary process)


