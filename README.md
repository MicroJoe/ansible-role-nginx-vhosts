nginx vhosts role
=================

Activate and deactivate nginx vhosts using Ansible.

Role Variables
--------------

`vhosts_enabled`

A list of virtual hosts to be enabled.

The script will look for each file in `/etc/nginx/sites-available` and link it
to `/etc/nginx/sites-enabled`. Any link in `/etc/nginx/sites-enabled` that is
not in this list will be removed.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: MicroJoe.nginx-vhosts
           vhosts_enabled:
             - default
             - www.example.com.conf
           tags: [nginx-vhosts]

License
-------

MIT

Author Information
------------------

Romain Porte
