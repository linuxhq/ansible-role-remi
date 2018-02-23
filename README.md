# ansible-role-remi

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-remi.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-remi)

RHEL/CentOS - Remis RPM repository.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    remi_pkg: remi-release
    remi_rel: "{{ ansible_distribution_major_version }}"
    remi_baseurl: "https://rpms.remirepo.net/enterprise"
    remi_release: "{{ remi_pkg }}-{{ remi_rel }}"
    remi_fetch: "{{ remi_baseurl }}/{{ remi_release }}.rpm"
    remi_remi: false
    remi_remi_debuginfo: false
    remi_remi_safe: true
    remi_remi_safe_debuginfo: false
    remi_remi_test: false
    remi_remi_test_debuginfo: false
    remi_remi_php54: false
    remi_remi_php70: false
    remi_remi_php70_debuginfo: false
    remi_remi_php70_test: false
    remi_remi_php70_test_debuginfo: false
    remi_remi_php71: false
    remi_remi_php71_debuginfo: false
    remi_remi_php71_test: false
    remi_remi_php71_test_debuginfo: false
    remi_remi_php72: false
    remi_remi_php72_debuginfo: false
    remi_remi_php72_test: false
    remi_remi_php72_test_debuginfo: false

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.remi
          remi_remi: true

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
