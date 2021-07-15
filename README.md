### Create auth htpasswd file

```bash
docker run --rm -it xmartlabs/htpasswd username password >> auth/htpasswd
```
or 
```bash
sudo apt install -y apache2-utils
htpasswd -Bbn testuser testpassword >> auth/htpasswd
```

### Login to registry

```bash
docker login registry.localhost
```

### Error docker push command: unknown blob

If after docker push <image> viewing error `unknown blob`, 
set nginx conf `proxy_set_header X-Forwarded-Proto https`.

https://github.com/distribution/distribution/issues/2225#issuecomment-356882178