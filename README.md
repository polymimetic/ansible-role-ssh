# Ansible Role: Ssh

[![Build Status](https://img.shields.io/travis/polymimetic/ansible-role-ssh.svg?style=flat-square)](https://travis-ci.org/polymimetic/ansible-role-ssh)
[![Release](https://img.shields.io/github/tag/polymimetic/ansible-role-ssh.svg?style=flat-square)](https://github.com/polymimetic/ansible-role-ssh/releases)
[![License: MIT](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-polymimetic.ssh-blue.svg?style=flat-square)](https://galaxy.ansible.com/polymimetic/ssh/)

Generates SSH keys & configuration.

## Requirements

No requirements.

## Dependencies

No dependencies.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ssh_user: "{{ ansible_env.USER }}"

Default SSH user

    ssh_home: "{{ ansible_env.HOME }}"

Default SSH home directory

    ssh_privkey: "{{ ssh_home }}/.ssh/id_rsa"
    ssh_pubkey: "{{ ssh_home }}/.ssh/id_rsa.pub"

Default ssh public & private key files.

    ssh_key_comment: "{{ inventory_hostname }}"

SSH key parameter

## Example Playbook

To run the role, include it as follows:

    - hosts: all
      roles:
         - { role: polymimetic.ssh, x: 42 }

## Credits

This role takes inspiration from the following Ansible roles:

- [manala.ssh](https://github.com/manala/ansible-role-ssh)
- [tersmitten.ssh-keys](https://github.com/Oefenweb/ansible-ssh-keys)

## License

This software package is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the [LICENSE](./LICENSE) file for details.

## Author Information

This role was created in 2017 by [Polymimetic](https://github.com/polymimetic).

* ansible-role-ssh generated using [ansible-role-skeleton](https://github.com/polymimetic/ansible-role-skeleton)