# Role Name

An [Ansible](https://www.ansible.com) to install/configure a loki-promtail stack

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
