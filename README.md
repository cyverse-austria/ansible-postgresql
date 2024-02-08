# Playbook postgresql

```bash
# ping
ansible -i inventory-exmpl.yml -m ping all --user root

# run playbook
ansible-playbook -i inventory-exmpl.yml --user=root --become site.yml
```

# using the role (postgresql)

## Role Variables

| var-name            | default          | description                          |
| ------------------- | ---------------- | ------------------------------------ |
| postgresql_version  | 12               | postgres version to install          |
| postgresql_subnet   | 0.0.0.0/0        | subnet to reach the database         |
| postgresql_password | "changemeplease" | postgresPW should be set in pipeline |

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: postgresql
      postgresql_version: 12
      postgresql_subnet: "0.0.0.0/0"
      postgresql_password: "changemeplease"
```
