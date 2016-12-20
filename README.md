mongodb
=========

This role has been built for a dev environment for CentOS7, Debian Jessie and Ubuntu Trusty, with MongoDB 3.0 or 3.2.

Tested on CentOS7, Ubuntu Trusty and Debian Jessie, using Ansible 2.1



Role Variables
--------------

Main role variables in defaults/main.yml
Set version, interfaces, ports, db path and log path.
NOTE: changing db path requires SELinux permission updates if it's enabled.


```yml
mongodb_version: 3.2 # 3.0 or 3.2
mongo_replication_set: 'rs0' #!!null to disable
mongodb_interfaces: ['127.0.0.1']
mongodb_port: 27017
mongodb_storage_path: '/data/db'
mongodb_db_path: '/data/db'
mongodb_log_path: '/var/log/mongodb'
mongodb_authorization: 'enabled'
```

OS dependent variables set in vars/<os family>.yml

Useful links
------------

[ Mongodb installation manual](https://docs.mongodb.com/manual/installation/M)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: true
      roles:
         - mongodb

License
-------

MIT
