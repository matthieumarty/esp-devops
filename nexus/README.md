# Nexus

### Getting started
- give nexus permission to use data directory
```bash
sudo chown 200:200 data
```

- launch the stack
```bash
docker stack deploy nexus -c doker-compose.yml
```

- retrieve default admin credentials
```bash
cat ./data/admin.password
```

### Create Docker registry
- Go to settings > create repository > docker(hosted)
- Complete registry information:
```
Name: docker-registry
HTTP: 8082
Docker api: enabled
online: enabled
```

> To enable usage of unsecured registries (non https), go to /etc/docker/daemon.json and add the following parameters:
```json
"insecure-registries"
["185.217.125.124:8082"]
```

