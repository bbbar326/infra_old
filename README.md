# infra
Ansible test environments using Docker.

# Usage
``` shell
$ git clone git@github.com:bbbar326/infra.git
$ cd infra
$ docker-compose up -d
$ docker-compose exec controller /bin/bash

## in 'controller' (Docker container) ##

$ cd ansible
$ ansible-playbook ./setup.yml -vvv -i ./hosts
$ exit

## end ##

$ docker-compose exec target /bin/bash

## in 'target' (Docker container) ##

$ cat ~/now.txt

## end ##
```
