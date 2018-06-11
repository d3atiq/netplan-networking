netplan-networking
==================

A simple role for configuring network interfaces in a netplan-enabled machine (currently only Ubuntu 18.04)

Requirements
------------

None

Role Variables
--------------

A quick description of the variables is given in the defaults file.

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        interfaces:
        - interface: eth0
          ipv4:
            configured: true
            address: 10.0.0.10/8
            gateway: 10.0.0.1
          dns:
            nameservers:
            - 10.0.0.1
            - 10.0.0.2
            searchdomains:
            - example.com
            - intranet.example.com
        - interface: eth1
          ipv4:
            configured: true
          dns:
            nameservers:
            - 10.1.0.1
            - 10.1.0.2
            searchdomains:
            - example.com
            - intranet.example.com
      roles:
         - netplan-networking

License
-------

MIT

Author Information
------------------

Under construction...
