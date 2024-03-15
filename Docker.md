Born from the merge of 2 Linux-native technologies: Namespaces and Control Groups.

## Docker Namespaces available

| Namespace | Description                |
| --------- | -------------------------- |
| USERNS    | User lists                 |
| MOUNT     | Access to file systems     |
| NET       | Network communication      |
| IPC       | Interprocess communication |
| PID       | Process ID Management      |
| CGROUP    | Create Contro Groups       |
| UTC       | Create host/domain names   |
## Docker commands

### Docker container
Basic set of commands, has `crete` , `run` , `start` ...

- `docker container start ID` : to start a docker container you need to paste its hexadecimal ID string. If it prints it back after a few moments, the command ended properly (common in a lot of docker commands)

### Docker ps
`docker ps` lists all the dockers that are running. If you want to list all the dockers append `--all` or `-a`.
The status of a fresh container is "Created", but if it runned it will be e.g. "Exited (..)" with a status code. Status code = 0 means that it successfully exited into runtime, other status codes need to be investigated.

### Docker logs
Synthax: `docker logs ID` : you don't need to provide the entire ID, it's able to autocomplete it starting from a few initial characters.
- you can attach the log right after starting a container using the attach option in a start subcommand:
```Docker
docker container start ID --attach ID
```
### Docker run
Concatenates a `create` , a `start` and a `--attach`. The only difference is that it won't show you the ID of the container when starting.
- is often useful to background containers with `-d`
##### Port Binding
Mapping a port from within the container to one on the local host:
```Docker
docker run -d ID -p OUT_PORT:IN_PORT ID
```
where the binding is performed by the flag `-p` followed by the outside port and the inside port (outside = local machine, insider = in the docker) separated by " : ".
##### Volume mounting
Sort of like port binding, it maps a folder from within the container to one on the local host:
```Docker
docker run -d ID -v OUT_FOLDER:IN_FOLDER ID
```
where the mapping allows the files created in the inside folder to be created also in the outside folder.
With the same synthax you can also map files to files, and once the mounting is done, changes to the file inside the container will result in the same changes on the outside file.
\[WARN] if the outside file doesn't exist, docker will create a directory (outside) with the name provided for the non-existing file and any attempt to modify the inside file will fail.
### Docker build
Builds a docker image starting from a dockerfile.
e.g. 
	`docker build -t NAME PATH`
	`docker build --file FILE_NAME PATH
NAME = name of the image
PATH = context (directory with the files to be included in the image)
FILE_NAME = name of the dockerfile
### Docker network


## Docker synthax

If you want to build a container from a dockerfile, the synthax is the following:
- FROM tells docker which image, local or from internet (default: dockerhub), you want to base your dockerfile off of;
- LABEL contain additional data e.g. the mantainer;
- USER tells which user to use to run any command underneath it (default: root \[DANGEROUS] ). You usually end with a less powerful user than `root`, so the last USER statement should be something else;
- COPY copies files from a directory (called _Context_) provided in a Build command to the container image;
- RUN is (most often _are_) a command used to customize your image e.g. install additional software like bash or configuration files;




Tags: Image tags specify the OS
``` Docker 
docker container create xxx:linux
```

