Role Name
=========

An Ansible role that installs Kibana 4.x on Red Hat / CentOS

Requirements
------------

This role was made to work with Nginx; other HTTP servers are not supported at
this time.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

* geerlingguy.nginx
* geerlingguy.repo-epel

Example Playbook
----------------

    - hosts: logging
      roles:
         - { role: 'geerlingguy.nginx' }
         - { role: 'geerlingguy.repo-epel' }
         - { role: 'leifmadsen.kibana-4' }

License
-------

Copyright 2016 Red Hat, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Author Information
------------------

This role was created in 2016 by [Leif Madsen](http://leifmadsen.com).
🐦 [@leifmadsen](http://twitter.com/leifmadsen)
