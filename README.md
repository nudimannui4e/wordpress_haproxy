## docker + wordpress + haproxy

1. Subnet for docker:

```
 sudo docker network create haproxy --subnet=172.172.0.0/24
```

2. (Optional) Portainer

```
docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```

3. run docker-compose

```
git clone https://github.com/nudimannui4e/wordpress_haproxy.git {folder}
cd {folder}
docker-compose up -d
```
