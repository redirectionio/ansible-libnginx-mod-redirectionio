# Ansible redirectionio-nginx_module role

This role installs the [redirection.io](https://redirection.io/) nginx module. It supports Debian and RHEL-based Linux distributions.

Once installed, the [redirection.io](https://redirection.io/) nginx module might be used in nginx Virtualhosts, as
described [in the related documentation](https://redirection.io/documentation/developer-documentation/nginx-module).

## Installation

Simply run the following command:

```
ansible-galaxy install redirectionio.nginx_module
```

## Role vars

This role does not provide variables.

## Example playbook

```yml
- hosts: webservers
  roles:
    - { role: redirectionio.nginx_module, become: true }
```

## Dependencies

This role has no dependency.

## License

This role is available under the terms of the MIT License.
