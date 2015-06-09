ansible-release
===========
[![Build Status](https://travis-ci.org/futurice/ansible-release.svg?branch=master)](https://travis-ci.org/futurice/ansible-release)

Provide project structure configuration.


Role Variables
--------------
```yaml
---
app_name: helloworld
www_root: "/var/www/"
project_path: "{{www_root}}{{app_name}}/"
timestamp: "{{ansible_date_time.epoch}}"
release_path: "{{project_path}}releases/{{timestamp}}/"
release_current: "{{project_path}}current"
virtualenv_path: "{{project_path}}venv/"
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: futurice.release }

License
-------

BSD
