# Ansible Role: traefik

[![Build Status](https://travis-ci.org/sbaerlocher/ansible.traefik.svg?branch=master)](https://travis-ci.org/sbaerlocher/ansible.traefik) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-traefik-blue.svg)](https://galaxy.ansible.com/sbaerlocher/traefik)

## Description

Installs and configures traefik as a docker container on a Linux docker environment.

## Installation

```bash
ansible-galaxy install sbaerlocher.traefik
```

## Use your own Traefik configuration template

Although the template packaged with this role can be configured using variables, you may want to use your own Traefik configuration file:

1. Create a `templates` directory at your playbook level
2. Create a `templates\traefik-conf.toml.j2` file (choose a different name from the default template `traefik.toml.j2`)
3. Set the var `traefik_configuration_template` to `traefik-conf.toml.j2` in your playbook

## Requirements

None

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| traefik_sendanonymoususage | false | |
| traefik_debug | false | |
| traefik_dir | /etc/traefik | |
| traefik_hostname | "{{ inventory_hostname }}" | |
| traefik_https | false | |
| traefik_https_redirect | false | |
| traefik_log_level | ERROR | |
| traefik_network | traefik_default | |
| traefik_api | false | |
| traefik_ping | false | |
| traefik_configuration_file | default provided | |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.traefik
```

## Changelog

### 1.0.0

* inital commit

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2018, Simon Bärlocher