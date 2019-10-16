Role Name
=========

VictoriaMetrics

Role Variables
--------------

```
---
victoriametrics_repo_url: "https://github.com/VictoriaMetrics/VictoriaMetrics"
victoriametrics_download_url:  "{{ victoriametrics_repo_url }}/releases/download/{{ victoriametrics_version }}/victoria-metrics-{{ victoriametrics_version }}.tar.gz"
victoriametrics_version: "v1.28.0"
victoriametrics_system_user: "victoriametrics"
victoriametrics_system_group: "{{ victoriametrics_system_user }}"
victoriametrics_delete_auth_key: "secret"
victoriametrics_snapshot_auth_key: "secret"
victoriametrics_service_args: ""
```


Example Playbook
----------------

```
- hosts: servers
    roles:
        - "ansible-victoriametrics-role"
```

Tests
------------
```
# deps
gem install kitchen-ansible --no-document
gem install kitchen-vagrant --no-document

# test
kitchen converge

```

License
-------

BSD

Author Information
------------------

sre@dreamteam.gg
