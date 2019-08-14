# Ansible redirectionio-nginx_module role

redirection.io is a Web traffic redirection manager. It provides a collection of tools for website administrators, SEO agencies and developers, which help analyze HTTP errors, setup HTTP redirections and monitor the traffic efficiently.

This role installs the [redirection.io](https://redirection.io/) nginx module. It supports Debian and RHEL-based Linux distributions.

Once installed, the [redirection.io](https://redirection.io/) nginx module might be used in nginx Virtualhosts, as
described [in the related documentation](https://redirection.io/documentation/developer-documentation/nginx-module#configuration).

## Installation

Simply run the following command:

```
ansible-galaxy install redirectionio.nginx_module
```

## Role variables

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
