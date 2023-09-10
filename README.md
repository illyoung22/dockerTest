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