# Docker Compose Deployment Guide

## 1. What Does the `services:` Block Do?

The `services:` block defines the containers that make up an application. In this project, it defines two services: `database`, which uses the `mariadb:10.6` image, and `app`, which uses the `nextcloud` image. Docker Compose uses this configuration to create and manage both services.

## 2. How Does Nextcloud Find MariaDB?

The Nextcloud application uses the following environment variable:

```yaml
- MYSQL_HOST=database
```

The value `database` matches the service name defined in the Compose file. Docker Compose provides network connectivity and service-name discovery so the Nextcloud container can reach the MariaDB service using that name.

## 3. Docker Run vs. Docker Compose

The `docker run` command is commonly used to create and start an individual container by specifying its image and options directly in the command. Docker Compose uses a YAML configuration file to define multiple related services, their settings, and their connections. The command `docker-compose up -d` starts the services defined in that file in the background, making multi-container applications easier to deploy and manage.

## 4. Commands Executed

### Create the Project

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
```

### Deploy the Application

```bash
docker-compose up -d
```

### Check the Services

```bash
docker-compose ps
```

### Shut Down the Application

```bash
docker-compose down
```

## 5. Screenshots

- `screenshots/compose-deployment.png` — Deployment and running services.
- `screenshots/nextcloud-web.png` — Nextcloud installation page.
- `screenshots/compose-teardown.png` — Shutdown and container removal.

## 6. Infrastructure as Code

Infrastructure as Code (IaC) means defining infrastructure through configuration files instead of relying entirely on manual setup. Docker Compose applies this principle by describing the application's services in a YAML file that can be reused, reviewed, and maintained.
