# Work in Progress

This is still work in progress, and experimental. If you want to help please do so all ideas and suggestions are welcome.


# Elm Ansible Playbook

Elm Ansible Playbook should give you some advantage when configuring system for you're local development. This playbook
will build you a virtual system with Elm project inside it.

## Basic Setup

You need to install latest version of [VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html).

After installing vagrant you'll also need to install vagrant-bindfs package, you can do that with

`vagrant plugin install vagrant-bindfs`.

Note: 

Maybe you don't need to install `vagrant-bindfs`, on initial startup of the machine Vagrant will notify you.

## StarUp Elm project

Git clone the project in any folder you like, and from the core folder in this case it's `elm-ansible-playbook` run

`vagrant up --provision`

That will trigger Vagrant file and it will starting to setup VirtualBox for the iToucan system. `--provision` flag will trigger `orchestartion/ansible/vagrant.yml`, and Ansible will start with roles for the project.

### Running Virtual Environment

You can ssh inside the VirtualBox with command `vagrant ssh`. When you get inside you will be in

```
Welcome to Ubuntu 16.04.5 LTS (GNU/Linux 4.4.0-137-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

19 packages can be updated.
8 updates are security updates.

New release '18.04.1 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Fri Oct 26 13:02:39 2018 from 10.0.2.2
vagrant@vagrant:~$ 

```

You need to `cd /srv/`. Run `ls` once more and you will see

```
example.com/ logs/
```

folders. 

* `example` folder is the folder containing the Elm application.
* `logs` folder contains all the logs for the entire system

You need to `cd example.com/` and `ls` inside that folder. You will see 

```angular2html
elm.json  orchestration  README.md  run_vagrant.sh  src  Vagrantfile
```

This is the root of Itoucan project. One of the main folder in this project is `src` - this is the source of Elm project, all code components is in that folder, and this is where
you will spend you're time coding.

### Error Logging

Elm setup is logging all the system errors and they can be found in `logs` folder. Inside the
folder we have

* nginx_access_itoucan.log 
* nginx_error_itoucan.log

### Code Editing

You don't need to setup anything for the local code editing. You can simply user you're IDE of choice and edit code.
