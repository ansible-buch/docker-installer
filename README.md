# Docker Engine Installer

This is an Ansible-based installer for Docker Engine (formerly known as
Docker CE) on various Linux Platforms. It has been tested on:

- Debian 12
- Rocky Linux 9
- openSUSE Leap 15
- Ubuntu 24.04

But it should also work on older versions of these distributions.


## Installation prerequisites:

You will need `ansible` (installation: see [here](https://github.com/ansible-buch/install-ansible)) and (of course) `git`.


## Installation:

Clone this repository and ch'dir into project folder:

```
git clone https://github.com/ansible-buch/docker-installer.git
cd docker-installer
```

Then start the `install.yml`-playbook with root permissions; e.g.:

```
sudo ansible-playbook install.yml
```

If you want to put a non-root user into the `docker` group, just add
`-e docker_user=USERNAME`, e.g.;

```
sudo ansible-playbook install.yml -e docker_user=vagrant
```

After a while, you will have Docker and some additional software installed:
- [`ctop`](https://github.com/bcicen/ctop)
- ...


> :warning: We no longer install the old `docker-compose` program,
> but use the newer Docker Compose plugin.
