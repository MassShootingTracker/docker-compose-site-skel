# Install file for docker compose.

## Prerequisites. 

These instructions assume the following:

1. Docker is installed
2. docker-compose is installed

If not, please see [these instructions](https://docs.docker.com/compose/install/)

## Install

Clone this repo.

    git clone https://github.com/MassShootingTracker/docker-compose-site-skel.git

Create and run contaners by executing the following in the directory which contains **docker-compose.yml**

    docker-compose up -d

After the web application starts, populate the database. (dep: Python 3)

    ./bin/update-mst-data

# Configure

To configure the webserver edit `./etc/mst/local.json`

    sudo vi etc/mst/local.json

The default configuration is for a local or staging environment, read comments in `docker-compose.yml` to deploy a production server

# Control the application

To stop the applicaton:

    docker-compose stop

To start the application after it's been stopped:

    docker-compose start

To view the logs of the containers:

    docker-compose logs

To delete the containers (but not the images):

    docker-compose rm
