# Server Containers

This repository contains a set of docker containers, using docker-compose. All containers are pulled from their respective repositories (except one). This configuration (mostly) follows a micro service architecture, the only outlier is the fact that all traffic passed through a central Nginx container. The Nginx container used is from the following repository (it provides some additional features not included in the default Nginx container):

- https://github.com/JonasAlfredsson/docker-nginx-certbot

## Environmental Variables

All environmental variables are separated into their own env files. This does have some restrictions on characters. For certain password complexity requirements it may be necessary to define passwords in the docker-compose.yml file.

## Nginx Configuration

Nginx configurations is not included in this repository, however the following links can be used to set up the provided containers (as of the 22/08/21, these resources are valid but this may change with time):

- PhotoPrism: https://docs.photoprism.org/getting-started/advanced/nginx-proxy-setup/
- Jellyfin: https://jellyfin.org/docs/general/networking/nginx.html
- Nextcloud: https://docs.nextcloud.com/server/19/admin_manual/installation/nginx.html
