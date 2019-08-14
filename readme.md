Docker Compose LEMP stack for Laravel Framework
=
### Services in the stack:
* L - Linux (Alpine)
* E - Nginx
* M - MySQL
* P - PHP

## Notes:
This container is built and tested for a Windows Docker host configured for Linux containers.

## Setup:
1. Clone this repo.
2. Copy your source web files into the src directory.
3. Make sure to take a look at **data/nginx/sites-available/default.conf** and verify the path is correct for your project.
4. Start the container with `docker-compose up`

 ### Configs:
Config files and other data is stored in the **data/** folder:
* **data/nginx/sites-available/default.conf** NGINX server configuration file.
* **data/root/.bashrc** formatting and extra commands for the bash shell.
* **data/root/.firstsetup.sh** some extra packages to install on login.
* **data/mysql/*** MySQL database files.

## Usage:

### Startup
**Report to console:** `docker-compose up`
**or Headless:** `docker-compose up -d`

### Shutdown
`docker-compose stop`

### Remove
`docker-compose down`

### Connect to Bash
`docker exec -it docker-lemp-dev_web_1 /bin/bash`
