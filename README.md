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