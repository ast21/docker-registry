### Create auth htpasswd file

```bash
docker run \
  --entrypoint htpasswd \
  registry:2 -Bbn testuser testpassword > auth/htpasswd
```

then 

```bash
docker login registry.localhost
```