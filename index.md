# smart home - home labs - containers - ssl proxy - wordpress themes  

The title says it all:
that's what you will find in my github repositories.

## moe lab

This repository provides various Docker containers that are based
on docker-compose. Each of the containers can be fired up using

```bash
docker-compose up -d
```

All the applications are proxied via traefik 2.0 which takes care
of SSL encryption. Thus, all frontend applications are connected
to a frontend network called traefik_proxy while backend systems
are only connected to the backend network.

Since we are using Docker containers, this relies on external
networks that need to be created before using the docker-compose
files:

```bash
docker network create traefik_proxy
docker network create backend
```