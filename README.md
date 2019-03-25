#Mautic+Letsencrypt SSL on Docker

This repository is easy easy to use and ready to set up two steps system.

This combines following:
 Ngnix
 Letsencrypt SSL
 Mautic
 Mysql

 This is a two part set up and uses another open source set up by [Evert Ramos](https://github.com/evertramos)
 it's called [Web Proxy using Docker, NGINX and Let's Encrypt](https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion#web-proxy-using-docker-nginx-and-lets-encrypt)
 
 The set up is really easy and is required as first step of using this setup.
 
 The logic is to put a proxy in front which can use the SSL certificate from Letsencrypt and then we put Mautic and Mysql behind it.
 
 ## Step 1
 Set up [Web Proxy using Docker, NGINX and Let's Encrypt](https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion#web-proxy-using-docker-nginx-and-lets-encrypt)
 
 ## Step 2
 Clone this repository adjecent to the "docker-compose-letsencrypt-nginx-proxy-companion"
 so your directory structure looks like:
 - docker-compose-letsencrypt-nginx-proxy-companion
 - MauticSSLDocker
 
 ## Step 3
 * Enter directory and find "docker-compose.yml"
 * Edit this file according to your settings and configuration
 * Save and run `docker-compose up -d`
 
 This is it to set up the mautic behind Ngnix proxy secured via letsencrypt SSL certificate.
 
 ## Points to note
 * Don't forget to configure docker-compose.yml according to your preference
 * Volume mount is optional but is recommended for mysql
 * For more configurations you can visit official [dockerhub](https://hub.docker.com/) pages for [mysql](https://hub.docker.com/_/mysql) and [mautic](https://hub.docker.com/r/mautic/mautic/)