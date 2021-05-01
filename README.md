# go-webapp-ssl-docker-all-in-one

Containerized application (for example golang) with nginx, letsencrypt and docker-compose.

Quick start

```bash
cp .env.example .env
# NOTE: setup DNS for your domain
# NOTE: sets your email (for letsencrypt)

# launches certificate setup
make setup

# must be zero
docker inspect certbot --format='{{.State.ExitCode}}'

# run app via reverse proxy with ssl
make up
```

The reference to a source.
- https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose
- https://gist.github.com/maxivak/4706c87698d14e9de0918b6ea2a41015
- https://letsencrypt.org/docs/challenge-types/


TODO
- [ ] guide for renew
- [ ] more checks for the states of life cycle
