# Docker Command

### Docker install 

### Docker Image Pull
```
 docker pull nginx
```

### Docker Container Run
```
 docker run nginx
```

### Docker Container Run Background option
```
 docker run -itd nginx
```

### Docker Container Name
```
 docker run --name My-Nginx nginx
```

### Docker Container Port Set 
```
 docker run -p 80:80 -p 443:443 --name My-Nginx nginx
```

### Docker Container All Set 
```
 docker run -itd -p 80:80 -p 443:443 --name My-Nginx nginx

❯ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                      NAMES
39df648b00f1   nginx     "/docker-entrypoint.…"   26 seconds ago   Up 26 seconds   0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp   My-Nginx
```


### Docker Container execute Shell 
```
 docker exec -it My-Nginx sh
 docker exec -it My-Nginx bash

 ❯  docker exec -it My-Nginx bash
root@39df648b00f1:/#  docker exec -it nginx bash
```

### Docker Running container check
```
docker ps

> CONTAINER ID   IMAGE     COMMAND                  CREATED       STATUS              PORTS                                      NAMES
39df648b00f1   nginx     "/docker-entrypoint.…"   12 days ago   Up About a minute   0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp   My-Nginx
```

### Docker Image List Check
```
docker images 

❯ docker images
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
nginx        latest    f5a6b296b8a2   2 weeks ago   187MB
mysql        latest    99afc808f15b   6 weeks ago   577MB
``` 

### Docker Container stop and check
```
❯ docker stop My-Nginx
My-Nginx

❯ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED       STATUS                      PORTS     NAMES
e499e02ed708   mysql     "docker-entrypoint.s…"   11 days ago   Exited (0) 11 days ago                mysql-sample-container
39df648b00f1   nginx     "/docker-entrypoint.…"   12 days ago   Exited (0) 39 seconds ago             My-Nginx
```

### Docker Container Delete and check
```
❯ docker rm My-Nginx
My-Nginx
❯ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED       STATUS                   PORTS     NAMES
e499e02ed708   mysql     "docker-entrypoint.s…"   11 days ago   Exited (0) 11 days ago             mysql-sample-container
```