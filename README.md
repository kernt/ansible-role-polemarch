Polemarch [![Build Status](https://travis-ci.org/miguelenes/ansible-role-polemarch.svg?branch=master)](https://travis-ci.org/holms/ansible-fqdn)
====

Provisions Polemarch 

http://polemarch.readthedocs.io/en/latest/

Requirements
------------

Ansible version 2.0+

## Platforms

* Debian
* Centos

Role Variables
--------------


| Variable name | Variable Description | Default |
|---------------|----------------|---------|
|*polemarch_version*     | version to install | `0.0.9` |
|*polemarch_config_debug*         | debug enabled | `true` |
|*polemarch_config_log_level*         | log level (DEBUG, INFO, WARNING, ERROR) | `WARNING` |
|*polemarch_config_timezone*         | application timezone | `UTC` |
|*polemarch_config_projects_dir*         | directory to store projects | `{HOME}/projects` |
|*polemarch_config_db_engine*         | database engine | `django.db.backends.sqlite3` |
|*polemarch_config_db_name*         | database name / location | `{HOME}/db.sqlite3` |
|*polemarch_config_db_timeout*         | database timeout | `10` |
|*polemarch_config_cache_engine*         | cache engine | `inventory_hostname` |
|*polemarch_config_cache_location*         | cache location | `inventory_hostname` |
|*polemarch_config_locks_engine*         | locks engine | `inventory_hostname` |
|*polemarch_config_locks_location*         | locks location | `inventory_hostname` |
|*polemarch_config_rpc_connection*         | rpc connection | `inventory_hostname` |
|*polemarch_config_rpc_result_backend*         | rpc result connection | `inventory_hostname` |
|*polemarch_config_rpc_heartbeat*         | rpc heartbeat value | `inventory_hostname` |
|*polemarch_config_rpc_results_expiry_days*         | rpc results expiration days | `inventory_hostname` |
|*polemarch_config_rpc_concurrency*         | rpc concurrency | `inventory_hostname` |
|*polemarch_config_web_allowed_hosts*         | allowed hosts | `*` |
|*polemarch_config_web_static_files_url*         | static files url | `inventory_hostname` |
|*polemarch_config_web_rest_page_limit*         | rest page limit | `inventory_hostname` |
|*polemarch_config_uwsgi_processes*         | number of processes | `inventory_hostname` |
|*polemarch_config_uwsgi_threads*         | number of threads | `inventory_hostname` |
|*polemarch_config_uwsgi_static_map*         | static map | `inventory_hostname` |
|*polemarch_config_uwsgi_pid*         | process ID | `inventory_hostname` |
|*polemarch_config_uwsgi_daemonize*         | daemonize | `inventory_hostname` |

Example
-------

```
- hosts: all
  become: true

  roles:
    - { role: miguelenes.ansible-role-polemarch, polemarch_version: "0.0.9", polemarch_config_debug: "false" }
```

License
-------

GPL

Author Information
------------------

Miguel Enes (<carlos.miguel.enes@imotorbike.com>)
