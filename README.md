[![Build Status](https://travis-ci.org/chrisjohnson00/ansible-role-jackett.svg?branch=master)](https://travis-ci.org/chrisjohnson00/ansible-role-jackett)

Role Name
=========

This is an ansible role to install [**Jackett**][1] on Ubuntu 16.04

Requirements
------------

The role is self contained

Role Variables
--------------

The defaults can be found in `defaults/main.yml`.

the ones of interest to you will be `chrisjohnson00_jackett_version` and `chrisjohnson00_jackett_user`
 
 - `chrisjohnson00_jackett_version` is the version of [**Jackett**][1] to install.  This follows the versions found on the [**Jackett**][1] github project.  If you want to upgrade the version, just update the variable and re-run the role.
 - `chrisjohnson00_jackett_user` is the user used to run the service, this user will be created if it doesn't exist.

Dependencies
------------

None

Example Playbook
----------------

    - name: with yourself
      hosts: all
      roles:
        - { role: chrisjohnson00.jackett, tags: ["jackett"]}

License
-------

MIT

 [1]: https://github.com/Jackett/Jackett