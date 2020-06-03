# Ansible Role: traefik

This Ansible Role is deprecated, please migrate to [arillso.traefik](https://github.com/arillso/ansible.traefik) role, more detailed information about migrating can be found at [Link](https://github.com/arillso/ansible.traefik#compatibility-with--sbaerlocheransibletraefik)

## Description

Installs and configures traefik as a docker container on a Linux docker environment.

## Installation

```bash
ansible-galaxy install sbaerlocher.traefik
```

## Requirements

None

## Role Variables

| Variable                   | Default                    | Comments (type) |
| :------------------------- | :------------------------- | :-------------- |
| traefik_sendanonymoususage | false                      |                 |
| traefik_debug              | false                      |                 |
| traefik_dir                | /etc/traefik               |                 |
| traefik_hostname           | "{{ inventory_hostname }}" |                 |
| traefik_https              | false                      |                 |
| traefik_https_redirect     | false                      |                 |
| traefik_log_level          | ERROR                      |                 |
| traefik_network            | traefik_default            |                 |
| traefik_api                | false                      |                 |
| traefik_ping               | false                      |                 |

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

- inital commit

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2018, Simon Bärlocher
