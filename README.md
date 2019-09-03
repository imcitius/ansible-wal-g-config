
This role configures wal-g and puts scripts for Backup/Restore

Requirements
------------

none

Role Variables
--------------
```
# default path to put scripts to
walg_script_path: /var/lib/pgsql/bin

# default S3 bucket name
walg_bucket: "wal-g"

# default S3 bucket path prefix (folder)
walg_prefix: "backup"

# how much full backups to retain in the storage
postgresql_backups_retain: 14

# User PostgreSQL runs under
postgresql_admin_user: postgres

# Default admin db
postgresql_admin_db: postgres

# S3 credentials
s3cmd_secret_key: ""
s3cmd_access_key: ""

```

Dependencies
------------
none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible_wal_g_config }

License
-------

GPLv2

Author Information
------------------

Ilya Rubinchik (aka Citius)
