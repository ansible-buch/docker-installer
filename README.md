# Docker Engine Installer

This is an Ansible-based installer for Docker Engine (formerly known as
Docker CE) on various Linux Platforms. It has been tested on:

- Debian 10 + 11
- Rocky Linux 8 + 9, CentOS Stream 9
- openSUSE Leap 15
- Ubuntu 20.04 + 22.04


## Installation prerequisites:

You will need `ansible` (installation: see [here](https://github.com/ansible-buch/install-ansible)) and (of course) `git`.


## Installation:

Clone this repository and ch'dir into project folder:

```
git clone https://github.com/ansible-buch/docker-installer.git
cd docker-installer
```

Then start the `installer.yml` with root permissions; e.g.:

```
sudo ./installer.yml
```

> :warning: This requires your `ansible-playbook`-command to be installed
in `/usr/bin`. If you get an error here, please fix the first line ("shebang")
in `installer.yml`. (Use `type ansible-playbook` to see your installation path.)


If you want to put a non-root user into the `docker` group, just add
`-e docker_user=USERNAME`, e.g.;

```
sudo ./installer.yml -e docker_user=vagrant
```

After a while, you will have Docker and these additional tools installed:
- [`docker-compose`](https://github.com/docker/compose)
- [`ctop`](https://github.com/bcicen/ctop)
- [`reg`](https://github.com/genuinetools/reg)

