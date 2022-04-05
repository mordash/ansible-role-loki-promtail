# Role Name

An [Ansible](https://www.ansible.com) role to install/configure a [loki](https://grafana.com/oss/loki/)-[promtail](https://grafana.com/docs/loki/latest/clients/promtail/) stack

## Role Variables

```yaml
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
