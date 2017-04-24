Centos-ansible
==============

This is a CentOS 7 docker image with ansible.
Linters is also installed in order to work with kitchen
for test purpose.

Prerequisites
-------------

- Docker

Usage
-----

```text
docker pull yueyehua/centos-ansible
docker run \
  -d \                                           # daemonize
  --privileged \                                 # for systemd
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \          # for systemd
  --name ansible \                               # container name
  -h ansible \                                   # hostname
  yueyehua/centos-ansible
docker exec -ti ansible bash
[Do something here]
docker stop ansible
docker rm ansible
```
