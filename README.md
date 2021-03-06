
![nscale](https://raw.githubusercontent.com/nearform/nscale/67447192084bd398b94a58ef93451ab18a3bd27a/docs/images/logo.png)

[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/nearform/nscale?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

> A toolkit for application deployments and container management

__nscale__ is an open source project to configure, build and deploy a set of connected containers to constitute a working platform for distributed applications.

Need docs? Check out our
[wiki](https://github.com/nearform/nscale/wiki).

Checkout the [workshop](https://github.com/nearform/nscale-workshop) to learn and use nscale in your projects.

## Install

```sh
[sudo] npm install -g nscale
```

__nscale__ depends on [nodejs](http://nodejs.org/), [npm](http://npmjs.org/) and [git](http://git-scm.com/).

### Run boot2docker on Mac OS X

If you are on Mac OS X, you need to start [boot2docker](https://github.com/boot2docker/boot2docker)

```sh
boot2docker up
```

Follow the instructions given by boot2docker to set your DOCKER_HOST environment variable!

## Running nscale

```sh
nsd server start
```

If you are running on Linux, you need to add yourself to the `docker`
group before running any `nsd` command. To do that:

```sh
sudo usermod -G docker -a `whoami`
```

## Getting started
Ensure that your ~/.gitconfig settings include a username and email.

### Login

By default, login uses the username and email defined in ~/.gitconfig and that is all that is required.

```sh
nsd login
```

### Clone nscale demo

```sh
nsd system clone git@github.com:nearform/nscaledemo.git
```

### Build web container

```sh
nsd container build nscaledemo web
```

### Deploy nscale demo


Deploy the latest revision:

```sh
nsd revision deploy nscaledemo latest
```

or deploy any revision, by replacing \<revision_id\>
with the a revision shown by the revision list command.

```sh
nsd revision list nscaledemo
nsd revision deploy nscaledemo <revision_id>
```

### Open nscale demo in the browser

Get the boot2docker ipaddress from a terminal type:
  boot2docker ip

```sh
open http://<ipaddress>:8000
```

### Open web gui

```sh
open http://localhost:9000
```

### Logs

```sh
nsd server logs
nsd server logs api.log
nsd server logs web.log
```

### Help

```sh
nsd help
```

## License

Copyright (c) 2014 Nearform and other contributors

Licensed under the Artistic License 2.0
