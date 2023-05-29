mprov-ng.slapd
=========

Ansible Role to install, configure, and optionally load a backup ldif into the openldap server

Requirements
------------



Role Variables
--------------

see [defaults file](defaults/main.yml)

Dependencies
------------


Example Playbook
----------------
```yaml
- hosts: all
  remote_user: root
  roles:
    - ansible-slapd
```

License
-------

License
-------
[Apache](LICENSE)

Author Information
------------------

Notes
-----
This role will configure a slapd server, but only if /var/lib/ldap/ansible_configured does NOT exist.  If you run this role on a server that does not have this file, it ***WIILL*** blow away your ***ENTIRE*** ldap directory and replace it...  You have been warned...

To re-initialize a slapd instance from scratch, remove /var/lib/ldap/ansible_configured and kill slapd.  Then re-run this role.
