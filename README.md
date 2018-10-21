# Ansible Role: traefik

[![Build Status](https://travis-ci.org/sbaerlocher/ansible.traefik.svg?branch=master)](https://travis-ci.org/sbaerlocher/ansible.traefik) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-traefik-blue.svg)](https://galaxy.ansible.com/sbaerlocher/traefik)

## Description

Installs and configures traefik as a docker container on a Linux docker environment.

## Installation

```bash
ansible-galaxy install sbaerlocher.traefik
```

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