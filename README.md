Ansible Rethinkdb Role
===

# Variables
```
rethinkdb_user          : "rethinkdb"
rethinkdb_group         : "rethinkdb"
rethinkdb_directory     : "/var/lib/rethinkdb/default"
rethinkdb_pid           : "/var/run/rethinkdb/rethinkdb.pid"
rethinkdb_log           : "/var/log/rethinkdb"
rethinkdb_bind          : "all"
rethinkdb_http_port     : 9090
rethinkdb_machine_name  : "{{ inventory_hostname }}"
# Cluster not WORKING YET
rethinkdb_cluster       : "false"

# http://www.rethinkdb.com/docs/cluster-on-startup/
rethinkdb_config        :
    runuser             : "{{ rethinkdb_user }}"
    rungroup            : "{{ rethinkdb_group }}"
    pid-file            : "{{ rethinkdb_pid }}"
    directory           : "{{ rethinkdb_directory }}/{{ inventory_hostname }}"
    log-file            : "{{ rethinkdb_log }}"
    bind                : "{{ rethinkdb_bind }}"
    http-port           : "{{ rethinkdb_http_port }}"
    machine-name        : "{{ rethinkdb_machine_name }}"
```
