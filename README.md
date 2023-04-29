![thumb-csgo-test](https://raw.githubusercontent.com/LacledesLAN/gamesvr-csgo-test/master/.misc/thumb-csgo-test.png "thumb-csgo-test")

This repository is maintained by [Laclede's LAN](https://lacledeslan.com). Its contents are heavily tailored and tweaked
for use at our charity LAN-Parties. For third-parties we recommend using this repo only as a reference example and then
building your own using [gamesvr-csgo](https://github.com/LacledesLAN/gamesvr-csgo) as the base image for your
customized server.

## Linux Container

### Download

```shell
docker pull lacledeslan/gamesvr-csgo-test;
```

### Run Self Tests

The image includes a test script that can be used to verify its contents. No changes or pull-requests will be accepted
to this repository if any tests fail.

```shell
docker run -it --rm lacledeslan/gamesvr-csgo-test ./ll-tests/gamesvr-csgo-test.sh;
```

### Run Interactive Server

```shell
docker run -it --rm --net=host lacledeslan/gamesvr-csgo-test ./srcds_run -game csgo +game_type 0 +game_mode 1 -tickrate 128 +mapgroup ll_orange +map orangebox_warmup_day +sv_lan 1
```

## Getting Started with Game Servers in Docker

[Docker](https://docs.docker.com/) is an open-source project that bundles applications into lightweight, portable,
self-sufficient containers. For a crash course on running Dockerized game servers check out [Using Docker for Game
Servers](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/DockerAndGameServers.md). For tips, tricks,
and recommended tools for working with Laclede's LAN Dockerized game server repos see the guide for [Working with our
Game Server Repos](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/WorkingWithOurRepos.md). You can
also browse all of our other Dockerized game servers: [Laclede's LAN Game Servers
Directory](https://github.com/LacledesLAN/README.1ST/tree/master/GameServers).
