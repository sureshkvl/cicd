# cicd
cicd

## prerequisties:

- ubuntu vm and docker, docker-compose installed



## Installation:

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
cd concourse
sudo ./keys/generate
sudo docker-compose up -d


## Ports:

gitea - 80,2222
concourse : 8080
nexus - 8081, 8082, 8083, 8084, 8085, 8123


## UI

concourse(8080):

username/password: test

gitea(80):

first registered user will be admin (to be explored)
suresh/

nexus(8081):
admin
password will be in  nexus-data/admin.password






## References:
1. https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
2. https://docs.docker.com/compose/install/
