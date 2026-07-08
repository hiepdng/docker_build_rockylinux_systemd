# Building Docker image: Rocky Linux 9 with systemd

### Build your own image
```
bash
docker build -t rockylinux:9
```
or

### pull image from dockerhub
```
docker pull hiepdng/rockylinux_systemd:latest
```

### Run the Container
```
docker run -d --name my-rocky-container --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro rockylinux_systemd
```

### Basic docker commands:
```
$ docker pull <image_name>       – Pull an image from dockerhub
$ docker image ls                – List all locally stored Docker images on your host system
$ docker run -it -d <image_name> – Create & start a new Docker container from animage and runs it in the background
$ docker ps                      – List all currently running Docker containers on your system
$ docker ps -a                   – lists all Docker containers on your system, regardless of their current status. 
$ docker stop <contaierID>       – Gracefully shuts down a running Docker container
$ docker start <contaierID>      – Resumes and boots up stopped Docker container
```


