# Nagios

Nagios container with NRPE.

Also contains:
* [ssmtp](https://linux.die.net/man/8/ssmtp)
* [PagerDuty integration](https://github.com/PagerDuty/pagerduty-nagios-pl)
* [HipChat integration](https://github.com/hannseman/hipsaint)

## Base image

* [`phusion/baseimage`](https://hub.docker.com/phusion/baseimage/)

## Supported tags and respective `Dockerfile` links

* [`latest` (*Dockerfile*)](https://github.com/MiLk/docker-nagios/blob/master/Dockerfile)

## How to use this image

You can use the following `docker-compose.yml` file to run your container.

```yaml
nagios:
  restart: always
  image: milk/nagios:latest
  ports:
    - 8000:80
  volumes:
    - ./etc:/opt/nagios/etc/
    - ./ssmtp:/etc/ssmtp
```

With that file, your nagios configuration files for nagios must be in `/opt/nagios/etc/`
and your ssmtp configuration files must be in `/etc/ssmtp`.

## Supported Docker versions

This image is officially supported on Docker version 1.12.3.

Support for older versions is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.