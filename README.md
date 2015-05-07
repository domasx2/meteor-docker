[![Dependency Status](https://www.versioneye.com/user/projects/551d7c9c971f7847ca000010/badge.svg?style=flat)](https://www.versioneye.com/user/projects/551d7c9c971f7847ca000010)
[![Dependency Status](https://www.versioneye.com/user/projects/551d7ca6971f78433900000e/badge.svg?style=flat)](https://www.versioneye.com/user/projects/551d7ca6971f78433900000e)

Meteor with Docker
=====================================================
This is a seed repo intended to bootstrap meteor project development. It uses docker for dev environment and contains a small sample application.

Requirements
=============
Docker 1.6
Docker-compose 1.2

Stack
=============
* Meteor.js
* MongoDB 3


Installation
=============

Docker dev environent requires latest docker, see https://docs.docker.com/installation/

#### Mac
1. Install boot2docker and Docker Compose
```
brew install boot2docker docker-compose
```
2. Initialize and start up boot2docker
```
boot2docker init
```
```
boot2docker start
```
3. Configure your Docker host to point to your boot2docker image.
```
$(boot2docker shellinit)
```
You’ll need to run this for every terminal session that invokes the docker or docker-compose command. 

4. 
```
boot2docker ssh -Cfo ExitOnForwardFailure=yes -vnNTL 3000:localhost:3000
```

Build and run
=============

```sh
#build images
docker-compose build

#start containers
docker-compose up
```

App should be up on [http://localhost:3000](http://localhost:3000/)

