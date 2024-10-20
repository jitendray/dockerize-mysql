# MySQL 8 Docker Setup with Docker Compose

This repository contains a Docker Compose configuration for setting up a MySQL 8 container with customizable options for volume storage and MySQL configuration using an `.env` file.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Commands](#commands)
- [Connecting to MySQL](#connecting-to-mysql)
- [Stopping the Container](#stopping-the-container)
- [License](#license)

## Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop) installed on your machine.
- [Docker Compose](https://docs.docker.com/compose/install/) installed (typically included with Docker Desktop).

## Getting Started

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/jitendray/dockerize-mysql.git
    cd dockerize-mysql
    ```

2. Update the .env file to set your environment variables.

##  Configuration
The Docker Compose configuration is defined in docker-compose.yml. It sets up a MySQL 8 container with:

- Environment variables loaded from the .env file.
- A bind mount for the MySQL data directory.
- A bind mount for the MySQL configuration file (my.cnf).


## Commands
**Start the MySQL Container**: To start the MySQL container in detached mode, run:
```bash
docker-compose up -d
```

**Check the Status**: To check if the MySQL container is running, use:
```bash
docker-compose ps
```

**Connect to MySQL**: To connect to the MySQL server using the command line, run:
```bash
docker exec -it mysql8 mysql -u root -p
```
Enter the root password you set in the .env file.

**Stop the Container**: To stop the MySQL container and remove it, run:
```bash
docker-compose down
```

## License
This project is licensed under the MIT License. See the LICENSE file for more information.
