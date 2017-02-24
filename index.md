---
layout: default
---
# [![klask.io](https://raw.githubusercontent.com/klask-io/klask-io/master/src/main/webapp/content/images/logo-klask.png)](https://github.com/klask-io/klask-io)

## What is klask.io ?
__[klask.io](https://github.com/klask-io/klask-io)__ is an open source search engine for source code. This application was generated using [JHipster](https://jhipster.github.io).

### Live demo
[app.klask.io](http://app.klask.io)

### How to run it with docker ?
You can run an instance easily by pulling the docker image and execute by following :

    docker run klask/klask.io

#### docker-compose
an example of a docker-compose.yml :

```Dockerfile
version: '2'
services:
  klask-app:
    image: klask/klask.io:latest
    ports:
      - 8080:8080
    volumes:
      - /mnt/svn:/repo
      - ./data:/klask-data
      - ./application-docker.yml:/application-docker.yml
```

`/mnt/svn` is the path to my repositories  
`./data` is the location where elasticsearch files and database were saved.  
The optional file `application-docker.yml` can overrides all properties defined in [application.yml](/src/main/resources/config/application.yml) and [application-docker.yml](/src/main/resources/config/application-docker.yml)   

