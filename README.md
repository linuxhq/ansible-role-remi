# ansible-role-remi

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-remi.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-remi)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-remi-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/remi)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Remis RPM repository.

## Requirements

This role requires that you have the epel repository installed.

 * https://galaxy.ansible.com/linuxhq/epel/

## Role Variables

Available variables are listed below, along with default values:

    remi_baseurl: "https://rpms.remirepo.net/enterprise"
    remi_disable_plugin: []
    remi_disablerepo: []
    remi_enable_plugin: []
    remi_enablerepo: []
    remi_fetch: "{{ remi_baseurl }}/{{ remi_release }}.rpm"
    remi_packages: []
    remi_pkg: remi-release
    remi_rel: "{{ ansible_distribution_major_version }}"
    remi_release: "{{ remi_pkg }}-{{ remi_rel }}"
    remi_repository_remi: false
    remi_repository_remi_debuginfo: false
    remi_repository_remi_php54: false
    remi_repository_remi_php55: false
    remi_repository_remi_php55_debuginfo: false
    remi_repository_remi_php56: false
    remi_repository_remi_php56_debuginfo: false
    remi_repository_remi_php70: false
    remi_repository_remi_php70_debuginfo: false
    remi_repository_remi_php70_test: false
    remi_repository_remi_php70_test_debuginfo: false
    remi_repository_remi_php71: false
    remi_repository_remi_php71_debuginfo: false
    remi_repository_remi_php71_test: false
    remi_repository_remi_php71_test_debuginfo: false
    remi_repository_remi_php72: false
    remi_repository_remi_php72_debuginfo: false
    remi_repository_remi_php72_test: false
    remi_repository_remi_php72_test_debuginfo: false
    remi_repository_remi_safe: false
    remi_repository_remi_safe_debuginfo: false
    remi_repository_remi_test: false
    remi_repository_remi_test_debuginfo: false

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.remi
          remi_repository_remi: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
