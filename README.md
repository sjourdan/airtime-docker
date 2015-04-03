# Airtime Docker

This is an early attempt at a fully working [Airtime](https://www.sourcefabric.org/en/airtime/) [Docker](https://www.docker.com/) container.

The final goal is to split services into different containers and configure them with [Consul](https://consul.io/):

* icecast2
* PostgreSQL
* httpd

We're not quite there yet.

It's currently running on Ubuntu 14.04

## Build

```shell
    sudo docker build -t="sjourdan/airtime" .
```

## Docker Automated Build

When pushed to GitHub, the [Docker Hub](https://hub.docker.com) builds it automatically: [Airtime Docker Automated Build](https://registry.hub.docker.com/u/sjourdan/airtime-docker/)

The docker repository is then available by issuing:

```shell
    docker pull sjourdan/airtime-docker
```

## Run

```shell
    sudo docker run -d -p 443:443 --name airtime sjourdan/airtime
```

or directly from the Docker Hub

```shell
    sudo docker run -d -p 443:443 --name airtime sjourdan/docker-airtime
```

## Stop

```shell
    sudo docker stop airtime
```

## Access

The Airtime container will be available from [https://localhost](https://localhost:443).
