# docker-directorylister

> Docker for DirectoryLister -- A simple PHP directory lister

## DirectoryLister

* Fork from [DirectoryLister-2.72](https://github.com/DirectoryLister/DirectoryLister/tree/2.7.2)
* Add new theme `vpsmm` for pretty

### Preview

![](https://raw.githubusercontent.com/stuarthua/PicGo/master/tmp/Snipaste_2020-02-09_07-48-15.png)

## Supported Architectures

The architectures supported by this image are:

| Architecture | Tag |
| :----: | --- |
| x86-64 | amd64-latest |
| arm64 | arm64v8-latest |
| armhf | arm32v7-latest |

## Usage

Here are some example snippets to help you get started creating a container.

### docker

```
docker create \
  --name=directorylister \
  -e PUID=1000 \
  -e PGID=1000 \
  -p 80:80 \
  -v <path to data>:/data \
  -v <path to config>:/config \
  --restart unless-stopped \
  stuarthua/directorylister
```

### docker-compose

Compatible with docker-compose v2 schemas.

```
---
version: "2"
services:
  directorylister:
    image: stuarthua/directorylister
    container_name: directorylister
    environment:
      - PUID=1000
      - PGID=1000
    volumes:
      - /path/to/data:/data
      - /path/to/config:/config
    ports:
      - 8080:80
    restart: unless-stopped
```
