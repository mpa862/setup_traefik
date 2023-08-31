# Docker Compose Setup for Traefik Reverse Proxy

This repository contains a Docker Compose configuration for setting up Traefik v2.5 as a reverse proxy to manage and route incoming traffic to different services within your Docker environment. Traefik makes it easy to expose multiple services on different subdomains or paths, handle SSL certificates, and provide advanced routing capabilities.

## Prerequisites

Before using this Docker Compose setup, make sure you have the following:

- Docker installed on your machine or server.
- A registered domain name for which you can configure DNS records.
- An email address to use for Let's Encrypt SSL certificate generation.

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/nisibz/setup-traefik-with-docker.git
   cd setup-traefik-with-docker
   ```

2. Update the `docker-compose.yml` file with your specific configurations:

   - Replace `email@example.com` with your valid email address in the `traefik` service section. This email address will be used for Let's Encrypt certificate registration and renewal.
   - You can customize other Traefik configurations, such as entry points, certificates resolvers, etc., as needed.

3. Create a Docker network for Traefik:

   ```bash
   docker network create traefik-net
   ```

4. Run the following command to start the Traefik container and configure it as a reverse proxy:

   ```bash
   docker-compose up -d
   ```
