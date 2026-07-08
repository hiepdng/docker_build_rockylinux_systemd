# Building Docker image: Rocky Linux 9 with systemd

### Build your own image
`$ docker build -t rockylinux_systemd .`

or

### Pull image from dockerhub
`$ docker pull hiepdng/rockylinux_systemd:latest`


### Run the Container
```
$ docker run -d \
  --cgroupns=private \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:rw \
  rockylinux_systemd
  ```

### Basic docker commands:
```
$ docker pull <image_name>       – Pulls an image from dockerhub
$ docker image ls                – Lists all locally stored Docker images on your host system
$ docker run -d <image_name>     – Creates & starts a new Docker container from animage and runs it in the background
  docker run -it -d --name image_name <image_name>
$ docker ps                      – Lists all currently running Docker container IDs on your system
$ docker ps -a                   – lists all Docker container IDs on your system, regardless of their current status. 
$ docker stop <containerID>      – Gracefully shuts down a running Docker container
$ docker start <containerID>     – Resumes and boots up stopped Docker container

$ docker exec -it <containerID> bash – Opens an interactive command-line terminal (Bash) inside a Docker
                                       container that is already running.
```






