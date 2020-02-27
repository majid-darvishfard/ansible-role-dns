dns
===

Configure DNS setup for a Linux server.


Version
-------

* `1.0.0` --- initial version
* `master` --- latest development version

Requirements
------------

This role is limited to:

* Ubuntu 12.04
* Ubuntu 14.04
* Ubuntu 16.04
* Ubuntu 18.04 --- `systemd-resolved`
* CentOS 6
* CentOS 7
* CentOS 8

Role Variables
--------------

* `dns_servers` --- list of IPs for DNS servers, default `['8.8.8.8', '1.1.1.1']`
* `dns_dnssec` --- boolean value to enable DNSSEC, default `true`.
* `dns_domains` --- list of search domains, default `[]`

Dependencies
------------

None

Example Playbook
----------------

Variables are kept in the `host_vars` or `group_vars` folder usually. Defining everything in playbook is not recommended. This is just an example.

    - hosts: servers
      vars:
      roles: user
      dns_servers:
        - 8.8.8.8
        - 1.1.1.1

Testing
-------

Testing the role with Vagrant running on VirtualBox.

    cd tests
    vagrant up

Rerun tests.

    vagrant provision

Remove test VMs.

    vagrant destroy -f

License
-------

GPLv2+

Author Information
------------------

Arnulf Heimsbakk <aheimsbakk@met.no>

###### set vim: spell spelllang=en: