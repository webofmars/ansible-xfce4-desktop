Ansible Role: xfce4-desktop
=====================

Build status for this role: [![Build Status](https://travis-ci.org/webofmars/ansible-xfce4-desktop.svg?branch=master)](https://travis-ci.org/webofmars/ansible-xfce4-desktop.svg?branch=master)


This role installs and configures Xfce4 Desktop on Ubuntu and Debian platforms

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values

**Debian**

```
xfce4_login_manager: gdm
xfce4_debian_extra_packages: []
xfce4_debian_packages:
  - xserver-xorg
  - xfonts-base
  - task-xfce-desktop
  - {{ xfce4_login_manager }}
```

**Ubuntu**

```
xfce4_ubuntu_extra_packages: []
xfce4_ubuntu_packages:
- xserver-xorg
- xfonts-base
- xubuntu-desktop
- {{ xfce4_login_manager }}
```

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - role: webofmars.xfce4-desktop
```
This example will install Xfce4 Desktop.


License
-------

GPLv3


Author Information
------------------

Created by Frederic Leger / webofmars.
