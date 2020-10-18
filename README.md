
# CheckPoint Configuration Backup
This is a simple Ansible playbook to backup your CheckPoint firewall configuration.

## Requirements
```
* Ansible == 2.9.7
* Python == 3.6.8
* CentOs == 7
```

## Usage
```
ansible-playbook -i <INVENTORY> main.yml
```

## Tested on
* Full-Gaia: R80
* Embedded-Gaia: R77 

## Important notes
The authentication for this playbook is just a placeholder, you must configure this section to your enterprise solution. My suggestion would be to use the [URI module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/uri_module.html).

This playbook is based on [**cli_command**](https://docs.ansible.com/ansible/2.9/modules/cli_command_module.html) due to the lack of support from CheckPoint for Ansible modules.

This **is not** a snapshot of the device and this **is not** a policies backup.

## Owner
[Giancarlo Mora](mailto:giank.ma@gmail.com)