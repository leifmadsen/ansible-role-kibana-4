# Ansible Role: Kibana

An Ansible role that installs Kibana 4.x on Red Hat / CentOS.

## Requirements

This role was made to work with Nginx; other HTTP servers are not supported at
this time.

You'll also need the EPEL repository for access to the `python-passlib`
library. You can enable the EPEL repository by adding the
`geerlingguy.repo-epel` role to your playbook.

## Role Variables

All available variables are listed below, along with their default values (see
`defaults/main.yml`).

    kibana_server_name: logs.example.tld

FQDN or IP address of the Kibana server.

    kibana_nginx_access_log: /var/log/nginx/kibana-4.access.log

Path and filename of the Nginx access log.

    kibana_version: 4.5

Major version of Kibana to install.

    kibana_username: kibana
    kibana_password: password

Kibana basic HTTP authentication username and password. You should update these
to be secure and not default.

## Dependencies

* geerlingguy.nginx
* geerlingguy.repo-epel

## Example Playbook

    - hosts: logging
      roles:
         - { role: 'geerlingguy.nginx' }
         - { role: 'geerlingguy.repo-epel' }
         - { role: 'leifmadsen.kibana-4' }

## License

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

## Author Information

This role is heavily influenced by the various
[geerlingguy](https://github.com/search?q=user%3Ageerlingguy+ansible-role)
Ansible roles, primarily the `geerlingguy.kibana` role (Kibana 3.x).

Created in 2016 by [Leif Madsen](http://leifmadsen.com).
🐦 [@leifmadsen](http://twitter.com/leifmadsen)
