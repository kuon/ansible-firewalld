firewalld
======

Simple role to manage firewalld rules (port opening)

Requirements
------------

none

Role Variables
--------------

- `port` - The port to open
- `public` - If set to true, the port will be open to the world
- `allowed_ips` - Instead of setting public to true, you can pass a list of ipv4 address to allow

Dependencies
------------

none

Example Playbook
----------------


    - hosts: servers

      roles:
      - { role: firewalld, port: 80, public: true }
      - { role: firewalld, port: 8080, allowed_ips: ['192.168.1.23'] }



License
-------

MIT

