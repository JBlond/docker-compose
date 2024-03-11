# docker-scale-demo

```
internet<--->openresty<----------->traefik/whoami
                        \  \  \
                         \  \  \-->traefik/whoami
                          \  \---->traefik/whoami
                           \------>traefik/whoami
```
