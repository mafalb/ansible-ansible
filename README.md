# An ansible role for ansible and it's dependencies.   [![Build Status](https://www.travis-ci.com/mafalb/ansible-ansible.svg?branch=master)](https://www.travis-ci.com/mafalb/ansible-ansible)

## Basic Usage

```
- hosts: localhost
  roles:
    - role: ansible
```

```
- hosts: localhost
  roles:
    - role: ansible/host
```

The latter will only install dependencies needed on an ansible node, not ansible itself.



## Variables

```
ansible_install_latest: false
```
If ansible is already installed, setting this to true will upgrade ansible to the latest version.

```
ansible_install_in_check_mode: true
```
e.g. check mode for the apt module on Debian-ish OS requires python-apt. Obviously this module is for installing such dependencies. Therefore, check mode for this module could fail. You could specify `check_mode: false` for the whole play, or you specifiy this variable which is setting the relevant package install section to `check_mode: false`
