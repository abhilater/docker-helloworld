# A Hello World! app on docker container

Table of Contents
==================
- [Steps to run](#steps-to-run)
- [Run with a mounted volume](#run-with-a-mounted-volume)


Steps to run
=============

1. Build the container image

```bash
docker build -t helloworld .
```

2. Run the container (container port 80 is forwared to host 8080)

```bash
docker run -p 8080:80 helloworld
```

3. Open http://localhost:8080


Run with a mounted volume
==========================

1. Mount host directory to container volume

```bash
docker run -p 8080:80 -v /Users/Path/docker-helloworld/src:/var/www/html/ helloworld
```
