#  Use Docker for symfony application Development
## The idea of this application is: 
    - Setup docker for symfony application development 
## Images:
    - nginx:stable-alpine 
        - nginx is used as web server 
    -  mysql:8
        - is used for mysql databases
    -  node:latest
        - is used to build the assets  
        - It will install Jquery, SCSS, webpack 
    - php:8.2-rc-fpm
        - php 8.2 will use for server side scripting  
    - schickling/mailcatcher
        - will used as local email server 

## Structure:
    -
    |_ app - PHP Appliation 
    |_ mysql - MY SQL data directory 
    |_ nginx - Nginx configuratin file 
    |_ php - PHP Docker configuration file 

## Set Up the developer environment
    - git clone https://github.com/indikaaruna8/friends-finder-docker
    - git clone https://github.com/indikaaruna8/freinds-finder
    - mv ./freinds-finder/* ./friends-finder-docker/app/
    - docker-compose build
    - docker-compose up
    - docker-compose run --rm node-service yarn install
    - docker-compose run --rm node-service yarn encore dev --watch

## Browser the web 
    - http://localhost:8081/
     
