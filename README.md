<p align="center">
   <img src="https://i.imgur.com/nqkqdBz.png" width="400">
</p>

# Description

Docker using compose, configuration file with environment variables and creating a container :

- nginx 1.19.0

# Nginx Container Configuration

1. Expose ports

   - 80 e 443

2. Volume (Note: check if in the docker configuration -> shared drivers, the units are enabled)

   - Application: htdocs -> /usr/share/nginx/html
   - Logs: nginx/logs -> /var/log/nginx
   - Virtual Host: nginx/sites -> /etc/nginx/conf.d

# How to use

1. Clone the repository using the command:

```
$ git clone https://gitlab.com/jadilson12/docker-compose-nginx
```

2. Enter the folder docker-compose-postgres copy the files

```
$ cp env-example .env
$ cp docker-compose.yml-example docker-compose.yml
```

3. Run your container:

```
$ docker-compose up -d
```

4. Add the domains in the system hosts file.

```
   127.0.0.1 localhost
```

5. Open in browser

```
http://localhost
```

6. Access the container shell:

```
$ docker exec -it app-database sh
```

## Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/jadilson12/docker-compose-nginx/issues).

## Show your support

Give a ⭐️ if this project helped you!
