[![Docker CI](https://github.com/pmikus/docker-ansible/actions/workflows/CI.yml/badge.svg)](https://github.com/pmikus/docker-ansible/actions/workflows/CI.yml)


Docker images that contains ansible and/or any pre-requistes installed within the images.

## Supported tags and Dockerfile:

- [docker-ubuntu-20.04-ansible](https://github.com/pmikus/docker-ansible/blob/master/ubuntu-20.04/Dockerfile)
- [docker-ubuntu-22.04-ansible](https://github.com/pmikus/docker-ansible/blob/master/ubuntu-22.04/Dockerfile)
- [docker-ubuntu-23.04-ansible](https://github.com/pmikus/docker-ansible/blob/master/ubuntu-22.10/Dockerfile)

## How to use:

Pull:

```shell
docker pull pmikus/docker-ubuntu-22.04-ansible
```

Run it directly.

```shell
docker run -it pmikus/docker-ubuntu-22.04-ansible /bin/bash
```

## Author:

Created by [Peter Mikus](https://www.linkedin.com/in/petermikus/).
