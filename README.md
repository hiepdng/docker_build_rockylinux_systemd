# Building Docker image: Rocky Linux 9 with systemd

### Build your own image
`$ docker build -t rockylinux:9`

or

### Pull image from dockerhub
`$ docker pull hiepdng/rockylinux_systemd:latest`


### Run the Container
`$ docker run -d --name my-rocky-container --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro rockylinux_systemd`


### Basic docker commands:
```
$ docker pull <image_name>       – Pulls an image from dockerhub
$ docker image ls                – Lists all locally stored Docker images on your host system
$ docker run -it -d <image_name> – Creates & starts a new Docker container from animage and runs it in the background
$ docker ps                      – Lists all currently running Docker container IDs on your system
$ docker ps -a                   – lists all Docker container IDs on your system, regardless of their current status. 
$ docker stop <containerID>      – Gracefully shuts down a running Docker container
$ docker start <containerID>     – Resumes and boots up stopped Docker container

$ docker exec -it <containerID> bash – Opens an interactive command-line terminal (Bash) inside a Docker
                                       container that is already running.
```






