# Grafana/Loki/Promtail/Syslog in Synology DSM

## Basic Instructions

1. Clone this repo to `/volume1/docker/lablogs`
1. Change all config references to `synergy` to your own Synology device's hostname
1. Create a Container Manager 'Project' around this new path
1. Fire it up

## State of the State

Very much a work in progress. Pulled this together from numerous sources (below), so some things may currently be unused, later to be used or removed. However, this repo should always result in a working setup.

## Goals

Ultimately, I'm trying to get my lab servers and network to log to this. This will be Omada syslog output, as well as lab servers. Lab containers will have their own Grafana stack to send logs and metrics to.

## TODO

* dashboards & network tags
* TLS

## Sources

The following sources were vital to my assembling this yaml pile

* basic quickstart docker compose for full service
  * https://github.com/grafana/loki/blob/main/production/docker-compose.yaml
* much more robust service with indepth config examples
  * https://github.com/grafana/loki/blob/main/production/docker/docker-compose.yaml
* docker compose in DSM
  * https://github.com/matt8707/docker-compose-dsm
* docker compose syslog-ng & promtail setup
  * https://github.com/grafana/loki/issues/5677
