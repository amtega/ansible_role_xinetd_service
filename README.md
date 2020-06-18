# Ansible sudo role

This is an [Ansible](http://www.ansible.com) role to setup a concrete xinetd service.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: all
  roles:    
    - role: amtega.xinetd_service
      xinetd_service_name: echo
      xinetd_service_id: echo-stream
      xinetd_service_type: INTERNAL
      xinetd_service_disable: no
      xinetd_service_socket_type: stream
      xinetd_service_protocol: tcp
      xinetd_service_user: root
      xinetd_service_wait: "no"
```

## Testing

Tests are based on [molecule with docker containers](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.xinetd_service

molecule test
```

## License

Copyright (C) 2020 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.
