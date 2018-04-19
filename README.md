# gamesvr-srcds-csgo-test
Docker image for client-test [Counter-Strike: Global Offensive](http://store.steampowered.com/app/730/) servers.

# Linux Container
[![](https://images.microbadger.com/badges/version/lacledeslan/gamesvr-csgo-test.svg)](https://microbadger.com/images/lacledeslan/gamesvr-csgo-test "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/lacledeslan/gamesvr-csgo-test.svg)](https://microbadger.com/images/lacledeslan/gamesvr-csgo-test "Get your own image badge on microbadger.com")

## Download

```shell
docker pull lacledeslan/gamesvr-csgo-test;
```

## Run Self Tests

```shell
docker run -it --rm --net=host lacledeslan/gamesvr-csgo-test ./ll-tests/gamesvr-csgo-test.sh;
```

## Run Interactive Server

```shell
docker run -it --rm --net=host lacledeslan/gamesvr-csgo-test ./srcds_run -game csgo +game_type 0 +game_mode 1 -tickrate 128 +mapgroup ll_orange +map orangebox_warmup_day +sv_lan 1
```
