[![Build Status](https://travis-ci.org/chrisjohnson00/ansible-role-jackett.svg?branch=master)](https://travis-ci.org/chrisjohnson00/ansible-role-jackett)

Jackett
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
 
 
Contributing
-------

I use [vagrant][2] to test my changes on my local, in order to do this effectivly I need to create a symbolic link so ansible knows how to find the role under `./roles/chrisjohnson00.jacket`, on my local I do something like `ln -s ~/IdeaProjects/ansible-role-jackett ~/IdeaProjects/ansible-role-jackett/roles/chrisjohnson00.jackett`.  If you do choose to contribute, thank you, please ensure the tests pass before submitting a PR.

[1]: https://github.com/Jackett/Jackett
[2]: http://www.vagrantup.com