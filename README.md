ansible-role-user
=================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-user.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-user)

Manage users for CentOS 7 and Ubuntu 18.04

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - name: Test the User role for CentOS and Ubuntu systems
      hosts: user
      become: yes
      become_method: sudo
    
      vars:
        - user_list:
          - name: user01
            uid: 2001
          - name: user02
            ssh_key: ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCsizUbyTe...w== your_email@example.com
          - name: user03
            system: yes
          - name: user04
            state: absent
      roles:
        - ansible-role-user

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)