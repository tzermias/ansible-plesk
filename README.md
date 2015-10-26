ansible-plesk
=============

[![Build
Status](https://travis-ci.org/tzermias/ansible-plesk.svg?branch=master)](https://travis-ci.org/tzermias/ansible-plesk)
This role install Odin Plesk panel and runs the initial configuration script
along with some predefined variables. The role performs a typical installation
of Plesk components.

Role Variables
--------------
The most common variable that you would use is `plesk_release_id`, which
configures what version of Plesk should be installed. Currently, it defaults to
`PLESK_12_0_18` that will install Plesk 12.0.18. You can use `plesk_license` to
specify a valid Plesk license key and install it.

Variables for initial configuration of Plesk are also specified. In particular
the following variables are specified in `defaults/main.yml`

    plesk_admin_password: changeme
    plesk_email: test@mycompany.com
    plesk_hostname: server.myserver.com
    plesk_company: My Company
    plesk_name: Hosting Services
    plesk_phone: +1234567890
    plesk_address: Address Str. 1
    plesk_city: My City
    plesk_state: My State
    plesk_zip: 12345
    plesk_country: GR

Change `plesk_admin_password` to something more secure.

Example Playbook
----------------
To use this playbook, create a playbook with the following:

    - hosts: servers
      remote_user: root
      roles:
        - plesk

<!-- vi: tw=80 -->
