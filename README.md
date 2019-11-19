aaaaaaaa
# dockerfiles-centos-user-adderable
Centos7, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t fantablue1111/centos7 .
	docker run -it --name c1 -e USER=fantablue1111 -e PASSWD=fantablue1111 fantablue1111/centos7
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        fantablue1111/centos7      "/bin/bash"         7 seconds ago       Up 6 seconds                            c1
```

To test, ("fantablue1111" is username. )
```
	su - fantablue1111
```
To Rollback
```
    docker rm c1 -f
    docker rmi fantablue1111/centos7
```
