# docker-cloud-proxy [![](https://images.microbadger.com/badges/image/casestack/docker-cloud-proxy.svg)](https://microbadger.com/images/casestack/docker-cloud-proxy "Microbadger")

Status: **NOT MAINTAINED**

Easily access your services on a Docker Cloud (Tutum) stack in a deterministic manner.

## Intro

docker-cloud-proxy is an automated [docker-gen](https://github.com/jwilder/docker-gen) based proxy to [Docker Cloud](https://cloud.docker.com/)
services.

Simply add `casestack/docker-cloud-proxy` to your Docker Cloud cluster and access any of your service hostnames in the following formats:

```
<service>.<stack>.<domain>:<port>
<stack>.<domain>:<port>
```

```
web.helloworld.mydomain.com:80
redis.helloworld.mydomain.com:6379

# Same cluster, same node, different stack
stack2.mydomain.com:80
admin.stack2.mydomain.com:6379
api.stack2.mydomain.com:4444
api.stack2.mydomain.com:4445
```


You would have to enable a wildcard DNS record on your DNS server for `*.mydomain.com` to work.

## License

MIT
