# Vagrant Docker Swarm Cluster

![Badge de Licença](https://img.shields.io/badge/Vagrant-2.4.2-blue.svg?style=flat-square&logo=vagrant)
![Badge de Licença](https://img.shields.io/badge/Docker-27.2.0-blue.svg?style=flat-square&logo=docker)
![Badge de Licença](https://img.shields.io/badge/VirtualBox-7.1.4-blue.svg?style=flat-square&logo=virtualbox)
![Badge de Versão](https://img.shields.io/badge/app-v_1.0.0-green.svg?style=flat-square&logo=app)
![Badge de Status do Projeto](https://img.shields.io/badge/status-training-blue.svg?style=flat-square)

Create a local `Docker Swarm Cluster`

## Commands Vagrant

**`vagrant init`:** create `Vagantfile`
  
  - Edit Vagrantfile configurations

**`vagrant up`:** initialize Virtual Machines

**`vagrant destroy`:** remove all cluster nodes 

**`vagrant ssh <vm-name>`:** access Vitual Machine

**`sudo su`:** change for root mode

## Commands Docker

**`docker swarm init --advertise-addr <your-network-adapter-ip>`** for init a cluster

**`docker swarm join --token <swarm-token> ip:port`** to join nodes to the cluster

**`docker service create --name web-server --replicas 15 -p 8080:80 httpd`** create Apache Server replicated

**`docker service ls`:** list services running in cluster

**`docker service ps web-server`:** show web-server app distribution in cluster nodes

**`docker node update --availability drain <node-name>`:** node exits app distribution

**`docker node update --availability active <node-name>`:** node enter app distribution

**`docker volume create app`:** create a volume into container

**`cd /var/lib/docker/volumes/app/_data`:** navigation to volume folder

## Commands on `LEADER` node

**`apt install nfs-server -y`:** sync volume application 

**`exportfs -ar`:** send export notice

## Commands on `NO LEADER` node

**`[In node02] apt install nfs-common -y`:** allows no leader nodes listen export files on cluster