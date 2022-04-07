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

None

## Dependencies

None

## Example galaxy requirement

```yaml
---
#
# ansible-galaxy -r install requirements.yml
# or
# ansible-galaxy install -r requirements.yml
#
- src: https://github.com/mordash/ansible-role-loki-promtail.git
  version: main
  name: loki-promtail
```

## Example Playbook

```yaml
---
- hosts: all
  become: yes

  roles:
    - { role: loki-promtail,    tags: ['loki-promtail'] }

  vars:
    promtail_install: true
    promtail_haproxy_log: true
    promtail_apache2_log: true
```
