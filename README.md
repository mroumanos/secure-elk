# Secure ELK Stack (without X-PACK)

Contains a Dockerized stack for securing Kibana access using bitly's [oauth2 proxy](https://github.com/bitly/oauth2_proxy#environment-variables).
It uses NGINX's auth_request module and can really be used with any type of authentication backend, but OAuth2 is used in this case. If the backend 
it intended to be switched out, see more on the [auth_request](http://nginx.org/en/docs/http/ngx_http_auth_request_module.html) module. Simply said, 
the authentication backend would need to be passed some type of authentication token and return a 202 for approval...this would require making minor 
modifications to the nginx.conf file.

## Quickstart

- First, make a copy of the template: `cp docker-compose.proxy.template.yml docker-compose.proxy.yml`

- Edit docker-compose.proxy.yml with your OAuth keys (client, secret) and cookie key (generate one)

- Create SSL key pair (see [here](https://rietta.com/blog/2012/01/27/openssl-generating-rsa-key-from-command/)) and save key
as proxy/config/server.key and the certificate as proxy/config/server.crt 

- Run `docker compose -f docker-compose.yml -f docker-compose.proxy.template` and navigate to https://localhost
