# Ansible proxmox - role

This role provisioned a pve server on a plain debian installation.

## Variables in this role

* no_enterprise: bool (set to false if you have a valid enterprise subscription)
* manage_users_with_ansible: bool

## User Managment with this role

his role can create users and user groups. To be able to use this function, users and groups must be defined as follows:

```yaml
pve_groups:
  - name: group_name
    role: Administrator
    comment: "System Administrators"

users:
  - name: user_name
    pve_group: pve_admin
```