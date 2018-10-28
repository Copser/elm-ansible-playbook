Role Name [![Build Status](https://travis-ci.org/Copser/elm-ansible-role.svg?branch=develop)](https://travis-ci.org/Copser/elm-ansible-role)
=========

Ansible role for [Elm](https://elm-lang.org/) 


## Work in progress

Minimal example is ready, but this is still work in progress, need to tackle `elm install`, `elm make` state.

If you want to help, knock yourself out, thanks :)

Requirements
------------

None

Role Variables
--------------

You can check available variables in `vars/main.yml`. For now we are compiling elm from source so the only
variable for now are:

- wget
- curl

Dependencies
------------

None

Example Playbook (using default package)
----------------

    - hosts: servers
      roles:
         - copser.elm

License
-------

BSD

## Feedback, reports

are most [welcome](https://github.com/Copser/elm-ansible-role/issues)

Author Information
------------------

This role was created in 2018 by [Petar Pilipovic](https://twitter.com/Coopsess).

