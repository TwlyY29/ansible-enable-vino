Role Name
=========

Enables vino server for a certain user. This is requried to be able connect to Ubuntu 16.04

Requirements
------------



Role Variables
--------------

vino_user must be provided to specify which user this needs to be done.
In theory it could be done for current connected user according to dconf,
but when become specified it will be done for root.

Dependencies
------------

dconf module needs to be added to ansible repository.
For example if your ansible repository is in `/etc/ansbile`
then you can use
```
mkdir /etc/ansible/library
curl https://raw.githubusercontent.com/Alex2357/ansible-dconf/master/dconf.py > /etc/ansible/library/dconf
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: Alex2357.enable-vino, vino_user: 'john' }

License
-------

BSD


