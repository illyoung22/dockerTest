# SHELL SCRIPT
## How to exclude headers

### Docker list check
```
docker ps -a

CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS                      PORTS     NAMES
de78f80437bd   nginx     "/docker-entrypoint.…"   5 minutes ago   Exited (0) 15 seconds ago             EcsTest2
9fb2c7e7e88e   nginx     "/docker-entrypoint.…"   6 minutes ago   Exited (0) 15 seconds ago             EcsTest
```
### How to print only specific column values
```
docker ps -a | awk '{print $1}'

CONTAINER
2879d338a576
552384e70e0a
```
### When deleting Docker, even column names are included.
```
docker ps -a | awk '{print $1}' | xargs docker rm 

de78f80437bd
9fb2c7e7e88e
Error response from daemon: No such container: CONTAINER
```


### How to remove column name
```
docker ps -a | awk '{print $1}' | grep -v CONTAINER

2879d338a576
552384e70e0a
```
```
docker ps -a | grep -v CONTAINER

2879d338a576   nginx     "/docker-entrypoint.…"   2 minutes ago   Up 2 minutes   80/tcp                                      test2
552384e70e0a   nginx     "/docker-entrypoint.…"   2 minutes ago   Up 2 minutes   0.0.0.0:80->80/tcp, 0.0.0.0:50000->80/tcp   test
```
