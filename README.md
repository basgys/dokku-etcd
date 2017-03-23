# This repository is no longer maintained.

# dokku etcd (beta)

etcd plugin for dokku.

## disclaimer

This plugin is not production ready yet.

## requirements

- dokku 0.4.0+

## installation

```shell
# on 0.4.x
dokku plugin:install https://github.com/basgys/dokku-etcd.git etcd
```

## commands

```shell
etcd:create <name>         Create new ETCD container
etcd:destroy <name>        Destroy ETCD container
etcd:expose <name> [port]  Expose on a custom port if provided (random port otherwise)
etcd:link <name> <app>     Link etcd service to the app
etcd:logs <name> [-t]      Print the most recent log(s) for this service
etcd:restart <name>        Graceful shutdown and restart of the etcd service container
etcd:start <name>          Start a previously stopped etcd service
etcd:stop <name>           Stop a running etcd service
etcd:unexpose <name>       Unexpose a previously exposed etcd service
etcd:unlink <name> <app>   Unlink etcd service from the app
```

## usage

```shell
# create an etcd service named lolipop
dokku etcd:create lolipop

# another service can be linked to your app
dokku etcd:link lolipop playground

# you can tail logs for a particular service
dokku etcd:logs lolipop
dokku etcd:logs lolipop -t # to tail

# finally, you can destroy the container
dokku etcd:destroy lolipop
```

## contributing

Feel free to contribute to this project if you want to fix/extend/improve it.

## TODO

  - Implement/test etcd cluster
  - ...
