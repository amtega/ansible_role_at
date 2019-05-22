# Ansible amtega.at role

This is an [Ansible](http://www.ansible.com) role which restricts execution of
periodic tasks through 'at' command to root users.

## Requirements

[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Role Variables

There are no default variables. The role checks the files on the operating systems.

## Tests


## Dependencies

- [amtega.check_platform](https://galaxy.ansible.com/amtega/check_platform)
- [amtega.proxy_client](https://galaxy.ansible.com/amtega/proxy_client)
- [amtega.packages](https://galaxy.ansible.com/amtega/packages)

## Usage

<!-- Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too. For example: -->

This is an example playbook:

```yaml
---
- name: test amtega.at role
  hosts: vagrant_sandbox_vms
  roles:
    - role: amtega.packages
      vars:
        packages_os:
          all:
            all:
              at: present

    - role: amtega.at

```

## Testing

Tests are based on Vagrant machines.

Once you have a test machine, you can run the tests with the following commands:

```shell
$ cd amtega.at/tests
$ ansible-playbook main.yml
```

## License

Copyright (C) 2019 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Carlos Chedas Fernandez.
