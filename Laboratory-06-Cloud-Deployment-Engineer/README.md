# Laboratory 06: Cloud Deployment Engineer

## Mission Overview

This laboratory demonstrates how Docker Compose can deploy a multi-tier application using Nextcloud and MariaDB. I created a YAML configuration file to define the application and database services and deploy them together.

## Objectives

- Understand two-tier application architecture.
- Create a Docker Compose configuration file.
- Deploy Nextcloud and MariaDB containers.
- Verify the running containers.
- Access the Nextcloud web interface.
- Shut down the application stack.
- Document Infrastructure as Code using Markdown.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Understanding multi-tier architecture.
- Writing YAML configuration files.
- Using Docker Compose to deploy multiple containers.
- Connecting an application container to a database container.
- Accessing a web application through port mapping.
- Managing application deployment and teardown.
- Writing technical documentation using Markdown.

## Conclusion

This laboratory introduced me to Infrastructure as Code through Docker Compose. I learned how a single configuration file can define multiple services and simplify the deployment of a private cloud storage application.
