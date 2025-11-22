# Gitlab CI Demo
This demonstrate running gitlab job locally using `gitlab-ci-local`

## Commands

```sh
gitlab-ci-local --list
gitlab-ci-local hello_world_job
```

## Setup Container

```sh
docker run -it -v /var/run/docker.sock:/var/run/docker.sock --rm node:latest bash

apt update
apt install rsync vim docker.io -y
npm install -g gitlab-ci-local

git config --global user.name "Sagar Panda"
git config --global user.email "er.sagarpanda@gmail.com"

git clone https://github.com/sagarpanda/gitlab-ci-demo.git
gitlab-ci-local hello_world_job

```

## Python Job

```yaml
# .gitlab-ci.yml
image: python:3.11

build_job:
  script:
    - python --version
```