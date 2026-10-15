# Mission Reflection

This laboratory helped me understand how Docker Compose simplifies the deployment of applications that require multiple services. Instead of starting and configuring each container manually, I used a YAML file to define Nextcloud and MariaDB and deploy them together.

## 1. How Docker Compose Makes Deployment Easier

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because the configuration can be reused whenever the application needs to be deployed again. It also reduces the need to remember and type many separate commands. By using `docker-compose up -d`, I can start the services defined in the configuration file with a single command.

## 2. Importance of YAML Indentation

YAML uses indentation to show the relationship between configuration elements. If I use incorrect indentation or a Tab instead of spaces, Docker Compose may report a configuration error or interpret the structure incorrectly. This taught me to check the formatting carefully before deploying the application.

## 3. Purpose of Environment Variables

Environment variables provide configuration values to containers, such as database names, usernames, and passwords. In this project, Nextcloud uses these values to connect to MariaDB. They make configuration easier to manage, although real production deployments should use stronger credentials and secure secret-management methods instead of simple passwords in a file.

## 4. Deploying Nextcloud

Deploying a private cloud storage application in a few minutes showed me how useful containerization can be. I learned that an application can depend on multiple services, but Docker Compose helps connect and manage them through one configuration file. Seeing the Nextcloud installation page also helped me understand how infrastructure configuration becomes a working web application.

## 5. How My Understanding Has Evolved

Since Mission 1, my understanding of cloud computing has expanded from learning basic cloud concepts to practicing deployment and service management. I now understand that cloud engineers must consider how applications, databases, networking, and configuration work together. My GitHub portfolio is also becoming a record of practical exercises that demonstrate my growing technical knowledge.

## Conclusion

This mission introduced me to Infrastructure as Code and multi-container deployment. I gained a better understanding of how Docker Compose can make cloud deployments more consistent, organized, and easier to maintain.
