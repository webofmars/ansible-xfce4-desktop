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
webofmars_debian_xfce4_extra_packages: []
webofmars_debian_xfce4_packages:
  - xserver-xorg
  - xfonts-base
  - lightdm
  - task-xfce-desktop
```

**Ubuntu**

```
webofmars_ubuntu_xfce4_extra_packages: []
webofmars_ubuntu_xfce4_packages:
- xserver-xorg
- xfonts-base
- lightdm
- xubuntu-desktop
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