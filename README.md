plenv
=========

ansible role to install plenv, set local version and install Carton

Requirements
------------

require git and change settings able to git clone

Role Variables
--------------

* plenv_local

default is "5.24.1"

overwrite other vars file if you want to use other version

* app_user

default is "vagrant"

username of application user

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: dmanto.plenv, app_user: "username", plenv_local: "5.20.2"}


* cron or daemon

use templates/env.j2 if use perl script with daemon and cron

* crontab

```
SCRIPT=/path/to/env
* * * * $SCRIPT plenv exec perl script.pl
```

License
-------

BSD

Author Information
------------------

