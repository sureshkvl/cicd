# cicd
cicd

## prerequisties:
ubuntu vm and docker, docker-compose installed


1. start gitea
----------------
cd gitea
mkdir gitea-data
sudo docker-compose -f gitea.yaml up -d


2. start nexus
----------------
cd nexus
mkdir nexus-data
sudo docker-compose -f nexus.yaml up -d

3. start concourse
-------------------





Ports:

gitea - 8080, 2221
nexus - 8081, 8082, 8083, 8084, 8085, 8123
concourse : 8000

## References:
1. https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
2. https://docs.docker.com/compose/install/
