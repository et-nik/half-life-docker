[![License Apache 2.0](https://goo.gl/joRzTI)](https://github.com/et-nik/half-life-docker/blob/master/LICENSE)

![Half-Life Logo](http://files.gamebanana.com/img/ico/sprays/51f5acee815f0.png)

# Docker image for Half-Life Dedicated Server

### Build an image:

```
 $ make build
```

### Create and start new Half-Life server:

```
 $ docker run -d -p 27020:27015/udp -e START_MAP=stalkyard -e ADMIN_STEAM=0:1:1234566 -e SERVER_NAME="My Server" --name hl knik/hlds
```

### Stop the server:

```
 docker stop hl
```

### Start existing (stopped) server:

```
 docker start hl
```

### Remove the server:

```
 docker rm hl
```

### Use image from [Docker Hub](https://hub.docker.com/r/hlds/server/):

```
 $ docker run -d -p 27018:27018/udp -e PORT=27018 -e START_MAP=de_inferno -e ADMIN_STEAM=0:1:1234566 -e SERVER_NAME="My Server" --name hl knik/hlds +log
```
