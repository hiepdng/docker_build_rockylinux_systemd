# Building Docker image: Rocky Linux 9 with systemd

### Build your own image  
`$ docker build -t rockylinux_systemd .`


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

<br><br>
### Build Rocky Linux 9 with systemd and pre-installed utilies:
You can build images with provided Dockerfile files:

- **Dockerfile_Networking_Tools** - Rocky Linux with networking Tools installed\
```
$ docker build -f Dockerfile_Networking_Tools -t rockylinux_networkingtools .
$ docker run -d \
  --cgroupns=private \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:rw \
  rockylinux_networkingtools
```

- **Dockerfile_Development_Tools** - Rocky Linux with Development Tools installed\
```
$ docker build -f Dockerfile_Developement_Tools -t rockylinux_developementtools .
$ docker run -d \
  --cgroupns=private \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:rw \
  rockylinux_developementtools
```

- **Dockerfile_System_Tools** - Rocky Linux with System Tools installed\
```
$ docker build -f Dockerfile_System_Tools -t rockylinux_systemtools .
$ docker run -d \
  --cgroupns=private \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:rw \
  rockylinux_systemtools
```




