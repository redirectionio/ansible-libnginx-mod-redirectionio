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

By default, this role installs the last stable version of [libnginx-mod-redirectionio](https://github.com/redirectionio/libnginx-mod-redirectionio).
This behavior can be modified using the following role variables:

 * `redirectionio_nginx_module_channel` (default: `stable`): choose a specific release channel (`stable` or `beta`)
 * `redirectionio_nginx_module_main_version` (default: `2`): main version of the nginx module. This allows to upgrade safely your system without BC break with a new main version
 * `redirectionio_nginx_module_version` (default: `*`): specific version of the nginx module. Use `*` to use the latest available version. Valid versions are of the form: `[timestamp]:[version]-[build]`, if you want a specific version like `2.0.0`, you should use `:2.0.0-`

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
