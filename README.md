- hosts: all
  check_mode: false
  roles:
    - role: ansible/host

e.g. check mode on debian requires python-apt
you better had it installed in a previous play or your check mode will fail, if you do not specify check_mode: false
