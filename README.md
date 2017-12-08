# ansible-role-remi

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-remi.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-remi)

RHEL/CentOS - Remis RPM repository.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    remi_pkg: remi-release
    remi_rel: "{{ ansible_distribution_major_version }}"
    remi_baseurl: "http://rpms.famillecollet.com/enterprise"
    remi_release: "{{ remi_pkg }}-{{ remi_rel }}"
    remi_fetch: "{{ remi_baseurl }}/{{ remi_release }}.rpm"
    remi_remi: False
    remi_remi_debuginfo: False
    remi_remi_safe: False
    remi_remi_safe_debuginfo: False
    remi_remi_test: False
    remi_remi_test_debuginfo: False
    remi_remi_php55: False
    remi_remi_php55_debuginfo: False
    remi_remi_php56: False
    remi_remi_php56_debuginfo: False
    remi_remi_php70: False
    remi_remi_php70_debuginfo: False
    remi_remi_php70_test: False
    remi_remi_php70_test_debuginfo: False

All repositories are disabled by default.

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.remi
          remi_remi: True

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
