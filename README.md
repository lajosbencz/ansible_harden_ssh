# harden_ssh
### Ansible role to harden ssh

# Install

```
ansible-galaxy install lajosbencz.harden_ssh
```

# Usage

## Example playbook

```yaml
# pb.yml
---
- hosts: all
  gather_facts: false # important!
  vars:
    ansible_port: 5522
  roles:
    - role: lajosbencz.harden_ssh
```

```
ansible-playbook -i <inventory> pb.yml
```


## Reset to default port

```
ansible-playbook -i <inventory> pb.yml --extra-vars "ansible_port=5522 harden_ssh_port=22"
```
