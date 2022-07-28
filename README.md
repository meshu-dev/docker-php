# Docker setup for PHP / MySQL Development

This setup allows you to use docker and docker-compose easily for your development.

## Prerequisites

Go to user directory and open the .bashrc file

    vim ~/.bashrc
    
Add the following shorthand for the docker-compose command...

    # Docker
    alias dc='docker-compose'

## Setup

1. Open up terminal application and change to a directory where you want your docker dev setup, an example would be...

        cd ~/

2. Clone repository and then change directory to inside of the repository

        git clone git@github.com:meshu-dev/docker-php.git

        cd docker-php

3. Create docker network by running the following command...

        docker network create dev-network

4. Update hosts file with helloworld localhost domain...

        sudo vim /etc/hosts

        127.0.0.1   helloworld.docker

5. Create and run containers with the following command...

        dc up -d

6. Up open your web browser and go to http://helloworld.docker and the page should show the message "Hello World".

7. Start expanding the docker dev setup by adding your own services, check below to see commands on how to use setup.

___

## Docker compose commands

A full list of docker-compose commands can be found at [https://docs.docker.com](https://docs.docker.com/compose/reference").

Here is a list of common docker-compose commands you would use...

### Docker Compose - Up

Usage:

    dc up -d

Start up service docker containers.

___

### Docker Compose - Down

Usage:

    dc down

Shutdown service docker containers.

___

### Docker Compose - Build

Usage:

    dc build

Build service docker containers.
