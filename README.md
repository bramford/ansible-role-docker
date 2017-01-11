# Ansible Role: docker

Ansible role that installs docker, docker-compose and all required dependencies on Debian, RHEL/CentOS and Ubuntu.

## Supported Operating Systems

- RHEL/CentOS 6 (untested)
- RHEL/CentOS 7 (untested)
- Debian 7/8
- Debian 9 (current debian 'testing' release)
- Ubuntu 12.04+ (untested)

## Requirements

- Ansible 2.1+

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { docker }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with optional vars set
      hosts: all
      roles:
        - { docker,
            docker_users: ["derp"],
            docker_compose: no,
            docker_service_state: "stopped",
            docker_service_enabled: no
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/bramford/ansible-role-docker.git roles/docker
