## Descargar imagen


@juano20614 ➜ /workspaces/labs-docker-dev (main) $ docker pull ubuntu
Using default tag: latest
latest: Pulling from library/ubuntu
9c704ecd0c69: Pull complete 
Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest



## phython
juano20614 ➜ /workspaces/labs-docker-dev (main) $ docker pull python:3.9
3.9: Pulling from library/python
ca4e5d672725: Pull complete 
30b93c12a9c9: Pull complete 
10d643a5fa82: Pull complete 
d6dc1019d793: Pull complete 
c387064957b7: Pull complete 
26766ebde481: Pull complete 
8a42d17fd0e2: Pull complete 
79eda865cc8a: Pull complete 
Digest: sha256:fea84f3a3b72c41efe7fc3b07ae209c6856b852b942c05fa88b747b74f70e711
Status: Downloaded newer image for python:3.9
docker.io/library/python:3.9


## Ejecutar contenedor
@juano20614 ➜ /workspaces/labs-docker-dev (main) $ docker run -it ubuntu bash
root@af939145eeaa:/# 
root@af939145eeaa:/# ls -a
.  ..  .dockerenv  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var


## Eliminar contenedor
$ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS                        PORTS                                   NAMES
af939145eeaa   ubuntu    "bash"                   14 minutes ago   Exited (129) 8 seconds ago                                            compassionate_lewin
d10172e5b077   nginx     "/docker-entrypoint.…"   4 days ago       Exited (255) 21 minutes ago   0.0.0.0:8080->80/tcp, :::8080->80/tcp   hardcore_euler

@juano20614 ➜ /workspaces/labs-docker-dev (main) $ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
af939145eeaa946dbf222922c37ce14fdd4a37c8e47acb7d7b0a627078e4e06c
d10172e5b077f693b5b92bbbc1ad0b47884d11f124ca3888151893fa28b5e05d

Total reclaimed space: 1.101kB
