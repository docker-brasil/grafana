# Grafana docker image

[![Join the chat at https://gitter.im/docker-brasil/grafana](https://badges.gitter.im/docker-brasil/grafana.svg)](https://gitter.im/docker-brasil/grafana?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This container builds a container with the
latest master build of Grafana.

## Getting the image
    
    docker pull dockerbrasil/grafana


## Running your Grafana image
--------------------------

Start your image binding the external port `3000`.

   docker run -i -p 3000:3000 dockerbrasil/grafana

Try it out, default admin user is admin/admin.

## Configuring your Grafana container

All options defined in conf/grafana.ini can be 
overriden using environment variables, for example:

```
docker run -i -p 3000:3000 \
  -e "GF_SERVER_ROOT_URL=http://my-grafana-server.com"  \
  -e "GF_SECURITY_ADMIN_PASSWORD=secret"  \
  dockerbrasil/grafana
```
