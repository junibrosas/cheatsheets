Build a docker image from a Dockerfile:

```
docker build -t jbrosas/deploy-app .
```

Run container or image:

```
docker run --rm -d -p 3000:3000 kamaln7/node-hello-app
```

List the running containers:

```
docker ps
```

Stop the container by ID:

```
docker stop CONTAIENR_ID
```

Stop the container(s) using the following command:

```
docker-compose down
```

Delete all containers using the following command:

```
docker rm -f $(docker ps -a -q)
```

Delete all volumes using the following command:

```
docker volume rm $(docker volume ls -q)
```

Restart the containers using the following command:

```
docker-compose up -d
```

Remove all images:

```
docker rmi $(docker images -a -q)
```

Start a single service:

```
docker-compose up <service_name>
```

Stop a single service:

```
$ docker-compose stop <service_name>
```

Restart a single service:

```
$ docker-compose restart <service_name>
```

Build a single service:

```
$ docker-compose build <service_name>
```

Docker execute Redis CLI:

```
docker exec -it mail-cache-1 redis-cli
```

Run docker from parent directory

```
docker build -t external-api -f packages/external-api/Dockerfile .
```
