# Secure ELK Stack (without X-PACK)

Contains a Dockerized stack for securing Kibana access using bitly's [oauth2 proxy](https://github.com/bitly/oauth2_proxy#environment-variables).

## Quickstart

> First, make a copy of the template: `cp docker-compose.proxy.template.yml docker-compose.proxy.yml`
> Edit docker-compose.proxy.yml with your OAuth keys (client, secret) and cookie key (generate one)
> Run `docker compose -f docker-compose.yml -f docker-compose.proxy.template` and navigate to https://localhost