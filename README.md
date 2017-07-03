# Ansible sudo role

This is an [Ansible](http://www.ansible.com) role to setup a xinetd service.

## Requirements

- Ansible >= 2.3

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Dependencies

None.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: all
  roles:    
    - role: xinetd_service
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

Test are based on docker containers. You can run the tests with the following commands:

```shell
$ cd xinetd_service/test
$ ansible-playbook main.yml
```

If you have docker engine configured you can avoid running dependant 'docker_engine' role (that usually requries root privileges) with the following commands:

```shell
$ cd xinetd_service/test
$ ansible-playbook --skip-tags "role::docker_engine" main.yml
```

## License

Not defined.

## Author Information

- Juan Antonio Valiño García ([juanval@edu.xunta.es](mailto:juanval@edu.xunta.es)). Amtega - Xunta de Galicia
