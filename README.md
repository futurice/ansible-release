ansible-release
===============
[![Build Status](https://travis-ci.org/futurice/ansible-release.svg?branch=master)](https://travis-ci.org/futurice/ansible-release)

Provide project structure configuration.
Provide git deployment platter.


Role Variables
--------------
```yaml
---
release_name: helloworld
release_timestamp: "{{ansible_date_time.epoch}}"
release_prefix: "/var/www/"
release_root: "{{release_prefix}}{{release_name}}/"
release_path: "{{release_root}}releases/{{release_timestamp}}/"
release_current: "{{release_root}}current"
release_venv: "{{release_root}}venv/"

git_repo: false
git_branch: 'master'
```

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: futurice.release }

License
-------

BSD
