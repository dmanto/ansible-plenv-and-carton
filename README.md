# Ansible Role: install plenv and Carton

[![Build Status](https://travis-ci.org/dmanto/ansible-plenv-and-carton.svg?branch=master)](https://travis-ci.org/dmanto/ansible-plenv-and-carton)

Installs Perl development / production environment tools (plenv and Carton)  for RedHat/CentOS and Debian/Ubuntu linux servers.

## Requirements

None.

## Role Variables

* plenv_local

default is "5.24.1"

overwrite other vars file if you want to use other version

* app_user

default is "vagrant"

username of application user

## Dependencies

None.

## Example Playbook (creates user username, dir /home/username if not exists, with local perl 5.20.2)

    - hosts: servers
      roles:
        - { role: dmanto.plenv-and-carton, app_user: "username", plenv_local: "5.20.2"}


* cron or daemon

use templates/env.j2 if use perl script with daemon and cron

* crontab

```
SCRIPT=/path/to/env
* * * * $SCRIPT plenv exec perl script.pl
```

## License

MIT / BSD

## Author Information

This role was mainly inspired by ansible-role-java role written by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/), and swfz.plenv ansible role forked from github.

Author: Daniel Mantovani 2017
