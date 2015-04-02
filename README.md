# Airtime Docker

This is an early attempt at a fully working [Airtime](https://www.sourcefabric.org/en/airtime/) [Docker](https://www.docker.com/) container.

The final goal is to split services into different containers and configure them with [Consul](https://consul.io/):

* icecast2
* PostgreSQL
* httpd

We're not quite there yet.

## Build

    sudo docker build -t="sjourdan/airtime" .

## Run

    sudo docker run -d -p 443:443 --name airtime sjourdan/airtime

## Access

The Airtime container will be available from [https://localhost](https://localhost:443).
