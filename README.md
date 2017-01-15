# Install file for docker compose.

## Prerequisites. 

These instructions assume the following:

1. Docker is installed
2. docker-compose is installed

If not, please see [these instructions](https://docs.docker.com/compose/install/)

## Install

Clone this repo.

    git clone https://github.com/Praisebetoscience/shootingtracker.git

Checkout the docker-compose branch.

    git checkout docker-compose

Create and run contaners by executing the following in the directory which contains **docker-compose.yml**

    docker-compose up -d

After the web application starts, populate the database.

    update-mst-data

# Control the application

To stop the applicaton:

    docker-compose stop

To start the application after it's been stopped:

    docker-compose start

To view the logs of the containers:

    docker-compose logs

To delete the containers (but not the images):

    docker-compose rm
