# Ansible Role: docker_host

Install Docker Engine and some additional useful software

## Platforms / Tested on

Debian 11, Rocky 8, openSUSE 15, Ubuntu 20.04

## Role Variables

Available variables are listed below, along with default values:

    docker_user: # no default

    docker_compose_version: 1.29.2
    docker_ctop_version: 0.7.6
    docker_reg_version: 0.16.1

    docker_sdk: true

## Description

This role installs Docker Engine (formerly known as Docker CE)
from the repos hosted at docker.com. Only the SUSE package is taken
from the SUSE repository.

If you specify an account with `docker_user`, it will be put into the
`docker` group.

Additionally, the tools docker-compose, ctop and reg will be installed
directly from GitHub.
