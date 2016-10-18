# code-quality

##### Description
- Builds two containers:
  - sonarqube v5.6.3 (LTS)
  - mysql v5.6.x

##### Dependencies
- docker-compose
- docker client
- docker server

##### Commands

To build and run the container

```
$ cd <PATH>/ci-tools/code-quality
$ docker-compose build

You might need to run 
$ docker login docker.io

$ docker-compose up -d
```

To see the logs of the container

```
$ docker-compose logs
```

**To view the sonarqube UI**


1. grab the IP of the DOCKER_HOST - `docker-machine env <name of vm>`
1. utilize Browser (example) - `http://192.168.99.100:9000`
  - note: port is 9000


