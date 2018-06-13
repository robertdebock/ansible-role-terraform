terraform
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-terraform.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-terraform)

Provides terraform for your system.

Context
-------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/terraform.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.

Role Variables
--------------

You can configure ara using this structure:
```
ara_configuration:
  port:
    section: ara
    value: 8080
```

These are the settings you can use.

- dir
- database
- host
- port
- logconfig
- logfile
- loglevel
- logformat
- sqldebug
- ignore_parameters
- ignore_empty_generation
- ignore_mimetype_warnings
- playbook_override
- playbook_per_page
- result_per_page

Dependencies
------------

This role can be used to prepare your system:

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.3|ansible 2.4|ansible 2.5|
|------------|-----------|-----------|-----------|
|alpine-3.6|no|no|no|
|alpine-3.7|yes|yes|yes|
|archlinux|no|no|no|
|centos-6|no|no|no|
|centos-7|no|no|no|
|debian-buster|yes|yes|yes|
|debian-stretch|no|no|no|
|fedora-27|yes|yes|yes|
|fedora-28|yes|yes|yes|
|opensuse-42.2|no|no|no|
|opensuse-42.3|no|no|no|
|ubuntu-artful|yes|yes|yes|
|ubuntu-bionic|yes|yes|yes|

Example Playbook
----------------

The simplest way possible:
```
- hosts: servers

  roles:
    - robertdebock.bootstrap
    - robertdebock.ara
```

Install this role using `galaxy install robertdebock.update`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
