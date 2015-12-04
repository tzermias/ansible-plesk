ansible-plesk
=============

[![Build
Status](https://travis-ci.org/tzermias/ansible-plesk.svg?branch=master)](https://travis-ci.org/tzermias/ansible-plesk)


This role install Odin Plesk panel and runs the initial configuration script
along with some predefined variables. The role performs a typical installation
of Plesk components.

Role Variables
--------------
The most common variable that you would use is `plesk.release_id`, which
configures what version of Plesk should be installed. Currently, it defaults to
`PLESK_12_0_18` that will install Plesk 12.0.18. You can use `plesk.license` to
specify a valid Plesk license key and install it.

Variables for initial configuration of Plesk are also specified. In particular
the following variables are specified in `defaults/main.yml`

    admin_password: changeme
    email: test@mycompany.com
    hostname: server.myserver.com
    company: My Company
    name: Hosting Services
    phone: +1234567890
    address: Address Str. 1
    city: My City
    state: My State
    zip: 12345
    country: GR
    release_id: PLESK_12_0_18
    license: ""

Change `admin_password` to something more secure.

Example Playbook
----------------
To use this playbook, create a playbook with the following:

    - hosts: servers
      remote_user: root
      roles:
        - plesk

<!-- vi: tw=80 -->
