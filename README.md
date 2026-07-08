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

### Basic docker commands
- ```docker pull <dockerhub-image>```
- ```docker image ls```
- ```docker run```
- ```docker ps```
- ```docker ps -a```
- ```docker``


