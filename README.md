# LAMP Stack for HTL Krems
## Overview
This repository contains the Docker Compose configuration needed to quickly deploy a LAMP (Linux, Apache, MySQL, PHP) stack. The stack also includes PHPMyAdmin for MySQL management. This setup is encapsulated into three services: webserver, database, and phpmyadmin.

## Services
**webserver**: PHP 7.4 web server based on Apache
**database**: MySQL 8.0 database server
**phpmyadmin**: PHPMyAdmin instance to manage MySQL database

## Requirements
Docker
Docker Compose
## Features
Auto-restart on failure
Configurable port mappings
Extra hosts setting for Apache
Customizable configuration via environment variables
## Getting Started
Clone this Repository
```
git clone https://github.com/FlorianRauchberger/htllampdocker
```
Navigate to the Directory

```
cd htllampdocker
```
Start the Containers
```
docker-compose up -d
```

# Configuration
## Environment Variables
**HOST_APACHE_HTTP_PORT**: HTTP port for Apache. Default is 80.
**HOST_APACHE_HTTPS_PORT**: HTTPS port for Apache. Default is 443.
**HOST_MYSQL_PORT**: Port for MySQL. Default is 3306.
**HOST_PMA_PORT**: Port for PHPMyAdmin. Default is 81.
## MySQL
**MYSQL_ROOT_PASSWORD**: Root password for MySQL. Default is docker123.
**MYSQL_DATABASE**: Name of the default database created. Default is docker123.

## Extra Hosts
The Apache service is configured to recognize itself as lamp in addition to localhost. This is controlled by the extra_hosts setting.

## Development
The webserver service is configured to mount the files/apache directory as the document root. This allows you to develop locally and have the changes reflected in the container.