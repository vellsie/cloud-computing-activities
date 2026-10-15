# Multi-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture is an application design that separates an application into two main parts: the web/application tier and the database tier. These tiers communicate with each other to provide the complete service.

## The Web/Application Tier

The web/application tier handles user requests and provides the web interface. In this laboratory, Nextcloud runs in the application container and allows users to access the private cloud storage interface through a web browser. It communicates with the database to retrieve and store application information.

## The Database Tier

The database tier stores persistent application data, including user account information and file metadata. In this laboratory, MariaDB runs in a separate container and provides the database service used by Nextcloud.

## Why Separate Them?

Separating the web application and database into two containers makes the system easier to manage, update, and troubleshoot. Each service can be configured and maintained independently, while Docker Compose helps connect them. This separation also makes it easier to scale services when needed and avoids combining unrelated responsibilities in a single container.
