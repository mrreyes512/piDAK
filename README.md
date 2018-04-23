piDAK
=========

**Raspberry Pi - Docker - Ansible - Kubernetes**

A role designed to take a defaulted Raspberry Pi and get Kubernetes installed.

This role will:
  1. Set locale settings for Raspberry Pi and expand the file system
  2. Upgrade repo listing and Update packages
  3. Install custom packages
  4. Add new user and install ssh key for access
  5. Install Docker
  6. Assign Docker to Kubernetes cluster

Requirements
------------

Prior to executing playbook, you will have to etch a new image onto the SD card, and join the wifi network. I suggest using [Ethcer](https://etcher.io/) to re-image the card, and follow the walkthrough illustrating how to set up a [Headless Raspberry Pi Setup with Raspbian Stretch](http://frederickvandenbosch.be/?p=2385)

After your pi boots, you should be able to reach your pi with:
```bash
$ ping raspberrypi.local
$ ssh pi@raspberrypi.local
```

Place the Pi's IP address in the inventory file, and you should be able to execute the tasks in this role. 

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Acknowledgments and References
------------------------------

* [Etcher Wifi Preconfiguration](https://github.com/ccrisan/motioneyeos/wiki/Wifi-Preconfiguration)
* [Headless Raspberry Pi Setup with Raspbian Stretch](http://frederickvandenbosch.be/?p=2385)
