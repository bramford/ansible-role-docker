Ansible Role: docker
----------------------

[![Build Status](https://travis-ci.org/bramford/ansible-role-docker.svg?branch=master)](https://travis-ci.org/bramford/ansible-role-docker)

Ansible role that installs docker, docker-compose and all required dependencies on Debian, RHEL/CentOS and Ubuntu.


## Supported Operating Systems

- RHEL/CentOS 7 (Untested)
- Debian 8+
- Ubuntu 14.04+ (Untested)

## Requirements

- Ansible 2.8+

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { role: docker }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with optional vars set
      hosts: all
      roles:
        - { role: docker,
            docker_users: ["derp"],
            docker_compose: no,
            docker_service_state: "stopped",
            docker_service_enabled: no
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/tekniqueltd/ansible-role-docker.git roles/docker

## Acknowledgements
  * geerlingguy/ansible-role-docker
