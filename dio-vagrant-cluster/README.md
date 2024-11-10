![Badge de Licença](https://img.shields.io/badge/Vagrant-2.4.2-blue.svg?style=flat-square&logo=vagrant)
![Badge de Licença](https://img.shields.io/badge/Docker-27.2.0-blue.svg?style=flat-square&logo=docker)
![Badge de Licença](https://img.shields.io/badge/VirtualBox-7.1.4-blue.svg?style=flat-square&logo=virtualbox)
![Badge de Versão](https://img.shields.io/badge/app-v_1.0.0-green.svg?style=flat-square&logo=app)
![Badge de Status do Projeto](https://img.shields.io/badge/status-training-blue.svg?style=flat-square)

# Vagrant Docker Swarm Cluster
Create a local `Docker Swarm Cluster`

# Commands

**`vagrant init`:** create `Vagantfile`
  
  - Edit Vagrantfile configurations

**`vagrant up`:** initialize Virtual Machines

**`vagrant ssh <vm-name>`:** access Vitual Machine

**`sudo su`:** change for root mode

**`docker swarm init --advertise-addr <your-network-adapter-ip>`** for init a cluster

**`docker swarm join --token <swarm-token> ip:port`** to join nodes to the cluster

docker service create --name web-server --replicas 15 -p 8080:80 httpd

docker service ls

docker service ps web-server

docker node update --availability drain node01

docker node update --availability active node01

docker volume create app

cd /var/lib/docker/volumes/app/_data

apt install nfs-server -y

exportfs -ar

[In node02] apt install nfs-common -y 