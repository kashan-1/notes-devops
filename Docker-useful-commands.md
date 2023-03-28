## This file contains the docker useful commands

1. This commands is used to show the `running` docker containers
``` bash
docker ps
```

2. This commands is used to show the `all` containers\
  -a `list all containers(stoped & running)`
``` bash
docker ps -a
```
3. This command is used to `enter` in container(`terminal mode`)
``` bash
docker exec -it image_name bash
```
4. This command is used to run the docker container in `detach(run in background) mode`
``` bash
docker run -d image_name:tag
```

5. This command is used to run container and expose port\
    `[Host Port] : [Container Port]`\
    `-p` stands for `publish`
``` bash
docker run -p 9000:80 nginx:latest
```
6. `--name` is used to assign a name to container
``` bash
docker run --name container-name nginx:latest
```


``` bash
docker 
```
