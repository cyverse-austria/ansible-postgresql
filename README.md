# postgresql

```bash
# ping
ansible -i inventory-exmpl.yml -m ping all --user root

# run playbook
ansible-playbook -i inventory-exmpl.yml --user=root --become site.yml
```
