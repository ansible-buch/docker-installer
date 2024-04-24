# Ansible Role: docker_host

Install Docker Engine and some additional useful software

## Platforms / Tested on

Debian 12, Rocky 9, openSUSE Leap 15, Ubuntu 24.04

## Role Variables

Available variables are listed below, along with default values:

    docker_user: # no default

## Description

This role installs Docker Engine (formerly known as Docker CE)
from the repos hosted at docker.com. Only the SUSE package is taken
from the SUSE repository, because docker.com doesn't offer one.

The installation comes with a `daemon.json` where two features are enabled:

- json logging limited to 5 times 20 MB and compression
- live restore (allows daemon restarts without killing all containers)

If you specify an account with `docker_user`, it will be put into the
`docker` group, and therefore gets the permission to use Docker.

Additionally, the latest version of `lazydocker` will be installed directly
from GitHub.
