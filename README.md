# docker-apache-php-oracle
Docker Image built on Debian, with Apache2, PHP5.6, OCI8 extension and the Oracle Instant Client.

## Build the Docker image from github
    git clone https://github.com/humolot/Docker-Oracle-PHP.git
    cd Docker-Oracle-PHP
    docker build -t humolot/Docker-Oracle-PHP .

## Or pull the Docker image from Docker Hub
    docker pull humolot/Docker-Oracle-PHP

## Default Usage
Start a new container with the Apache2 Debian Default Page


    docker run -p 8080:80 -d humolot/Docker-Oracle-PHP

## Run the local sample page
Start a new container with the sample page containing a phpinfo(), and bind the port 80 of the container to port 8080 of your localhost.


    docker run -p 8080:80 -d -v $(pwd)/sample:/var/www/html humolot/Docker-Oracle-PHP

## Run your custom project
Start a new container with your application and bind the port 80 of the container to port 8080 of your localhost.


    docker run -p 8080:80 -d -v </local/path/www>:/var/www/html humolot/Docker-Oracle-PHP

## Test your deployment :
* Open [http://127.0.0.1:8080](http://127.0.0.1:8080) in your browser

## By
GoodBits Tech
