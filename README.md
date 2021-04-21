dudefellah.uwsgi
=========

This role installs and configures uwsgi for you.

Requirements
------------

None.

Role Variables
--------------

It's easiest to see what values are available by checking the comments
in [defaults/main.yml](defaults/main.yml). Each entry should be documented
there for you.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: webservers
      tasks:
        - block:
            - include_role:
                name: dudefellah.uwsgi
              vars:
                uwsgi_install_method: pip
                uwsgi_vassals:
                  - name: test
                    workdir: /opt/mytest
                    ...

License
-------

GPLv2+

Author Information
------------------

Dan - github.com/dudefellah
