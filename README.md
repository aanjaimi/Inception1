<h1 align="center">Inception</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/aanjaimi/Inception1?color=56BEB8">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/aanjaimi/Inception1?color=56BEB8">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/aanjaimi/Inception1?color=56BEB8">

  <img alt="License" src="https://img.shields.io/github/license/aanjaimi/Inception1?color=56BEB8">

  <!-- <img alt="Github issues" src="https://img.shields.io/github/issues/aanjaimi/Inception1?color=56BEB8" /> -->

  <!-- <img alt="Github forks" src="https://img.shields.io/github/forks/aanjaimi/Inception1?color=56BEB8" /> -->

  <!-- <img alt="Github stars" src="https://img.shields.io/github/stars/aanjaimi/Inception1?color=56BEB8" /> -->
</p>


<p align="center">
  <a href="#about">About</a> &#xa0; | &#xa0; 
  <a href="#features">Features</a> &#xa0; | &#xa0;
  <a href="#technologies">Technologies</a> &#xa0; | &#xa0;
  <a href="#requirements">Requirements</a> &#xa0; | &#xa0;
  <a href="#starting">Starting</a> &#xa0; | &#xa0;
  <a href="https://github.com/aanjaimi" target="_blank">Author</a>
</p>

<br>

## About ##

This project consists in a small infrastructure composed of different
services under specific rules using docker compose.
<br>
<br>
To export backup.sql from db container:
```shell
docker exec -it <mariadb_container_name> /bin/bash

mysqldump -u <user> -p <password> <db_name> > backup.sql

docker cp <mariadb_container_name>:/backup.sql /path/to/your/project/
```

## Features ##

• A Docker container that contains NGINX with TLSv1.2 or TLSv1.3 only.<br>
• A Docker container that contains WordPress + php-fpm (it must be installed and
configured) only without nginx.<br>
• A Docker container that contains MariaDB only without nginx.<br>
• A volume that contains WordPress database.<br>
• A second volume that contains WordPress website files.<br>
• A docker-network that establishes the connection between containers.<br>

## Technologies ##

The following tools were used in this project:

- [Docker](https://www.docker.com/)
- [Nginx](https://www.nginx.com/)
- [WordPress](https://br.wordpress.org/)
- [MariaDB](https://mariadb.org/)

## Requirements ##

Before starting, you need to have [Git](https://git-scm.com) and [Docker](https://www.docker.com/) installed.

## Starting ##

```bash
# Clone this project
git clone https://github.com/aanjaimi/Inception1

# Access
cd Inception1

# Run the project
make

# The server will initialize in the <https://aanjaimi.42.fr>

# To stop the project
make down

# To clean images and volumes
make clean

# To prune volumes, remove local data volume and restore the /etc/hosts
make fclean
```

<a href="#top">Back to top</a>
