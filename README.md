# Role Name

An [Ansible](https://www.ansible.com) role to install/configure a [loki](https://grafana.com/oss/loki/)-[promtail](https://grafana.com/docs/loki/latest/clients/promtail/) stack

## Default variables

### Promtail

```yaml
promtail_install: undefined
promtail_destination_server_port: 3100
promtail_haproxy_log_path: /var/log/haproxy/haproxy.log
promtail_apache2_log_path: /var/log/apache2/*/*.log
```

### Loki

```yaml
loki_install: undefined
loki_conf_template: ../templates/local-config.yaml.j2
loki_conf_path: /etc/loki
```

## Prerequisites

```
create user promtail on source server
```

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: all
  become: yes

  roles:
    - { role: loki-promtail,    tags: ['loki-promtail'] }
```
