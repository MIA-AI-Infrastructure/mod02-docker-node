# Simple project to start working with docker

It contains a node.js application.

Thanks to "Docker Up & Running 3rd Edition", O'Reilly



## Building

After downloading the source code and entering on the folder with the source code.

To build use the following command:

```
docker build -t mia-AI-infra/mod02-docker-node:v0.1 .
```

This builds the container with name mod02-docker-node with version v0.1



## Running

To image that was built, one can use the following command:

```
docker container run --rm -d -p 8081:3000 --name mod02-docker-node mia-AI-infra/mod02-docker-node:v0.1
```

*Note:* this creates a container to run the image in detach mode (background)

The running container can be confirmed with the command `docker ps`

The expected output is:

```
CONTAINER ID   IMAGE                                 COMMAND                  CREATED         STATUS         PORTS                                                      NAMES
fe7ca1328d64   mia-AI-infra/mod02-docker-node:v0.1   "docker-entrypoint.s&"   3 seconds ago   Up 3 seconds                                                              mod02-docker-node
```



## Stoping

```
docker stop mod02-docker-node
```

# Re-Running

```
docker start mia-AI-infra/mod02-docker-node
```
