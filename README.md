Ansible Role for Instaling git mirror
=========

This Ansible role installs git-daemon and sets up the directory where the mirrored repos would be stored. It is also adding a new user which will own these repositories and setting up a SSH keypair for him.

Requirements
------------

No Requirements are required for this role.

Role Variables
--------------

This role requires the following variables.

    service_file_destination: "/etc/systemd/system/"
    service_file_owner: root
    service_file_group: root
    service_file_mode: 0644
    service_file_listen_port: 9418
    repository_destination: "/var/lib/git"
    repository_owner: gitmirror
    repository_group: gitmirror


Dependencies
------------

This role is not dependent upon any galaxy roles.

Example Playbook
----------------

Here is a simple example of a git_mirror role:

    - hosts: servers
      roles:
         - git_mirror

License
-------

GNU GENERAL PUBLIC LICENSE

    Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc.

Author Information
------------------

This is developed by Satellite QE team, irc: #robottelo on Freenode
