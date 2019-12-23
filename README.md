# cicd

This is sample cicd stack with gitea, nexus and concourse


## 1.prerequisties:

- ubuntu vm , 4 Core, 16gb ram, 
- docker, docker-compose installed


## 2. Installation:

cd stack
sudo docker-compose -f gitea.yaml up -d
sudo docker ps -a


##3. configuration:

### Ports:

gitea - 80,2222
concourse : 8080
nexus - 8081, 8082, 8083, 8084, 8085


### Concourse UI

-concourse(8080)
-username/password: test


### Gitea configuration

- open the gitea UI(80)
- click the signin page, it will direct for config page
- do basic config, also create admin user.

### nexus(8081) Configuration
- login with user admin qnd password will be in  nexus-data/admin.password
- create a blob store named docker
- create a docker(hosted) registry, and make sure http proxy is enabled with port number 8082.
- from your laptop , login to this nexus docker registry (docker login)  and tag a image 'nexus:8082/test', make sure you are able to push it.




## 4. References:
1. https://blog.sonatype.com/using-nexus-3-as-your-repository-part-3-docker-images

1. https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
2. https://docs.docker.com/compose/install/
