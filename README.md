# parted


TODO: [![Build Status](https://travis-ci.org/cjsteel/ansible-role-parted.svg?branch=master)](https://travis-ci.org/cjsteel/ansible-role-parted)

The purpose of this role is to install and configure parted on your system.

TODO: [Unit tests](https://travis-ci.org/cjsteel/ansible-role-parted) are done on every commit and periodically.

If you find issues, please register them in [GitHub](https://github.com/cjsteel/ansible-role-parted/issues)

To test this role locally please use [Molecule](https://github.com/metacloud/molecule):

```shell
# Docker test:
pip install molecule ara
molecule test
# Vagrant tests
molecule test --scenario-name vagrant
```
There are many scenarios available, please have a look in the `molecule/` directory.

## Context

This role is a part of a collection of compatible roles.

## Requirements


- A target system or VM with the packages required to run Ansible.
- Access to any repository(ies) containing any required packages.
- A recent version of Ansible. (Created using Ansible 2.8.2)

## Role Variables

- parted_parameter: Description of values. [default: value]

## Dependencies


- None known.

## Compatibility


This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.8.2|ansible 2.9.|ansible 3.0|ansible 3.1|ansible devel|
|------------|-----------|-----------|-----------|-----------|-------------|
|alpine-edge*|||||*|
|alpine-latest|||||*|
|archlinux|||||*|
|centos-6|||||*|
|centos-latest|||||*|
|debian-latest|||||*|
|debian-stable|||||*|
|debian-unstable*|||||*|
|fedora-latest|||||*|
|fedora-rawhide*|||||*|
|opensuse-leap|||||*|
|ubuntu-artful|||||*|
|ubuntu-devel*|||||*|
|ubuntu-latest|||||*|

A single star means the build may fail, it's marked as an experimental build.

## Example Playbook


```yaml
---
- name: parted
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: cjsteel.bootstrap
    - role: cjsteel.parted
      parted_parameter: value
```

To install this role:
- Install this role individually using `ansible-galaxy install cjsteel.parted`

Sample roles/requirements.yml: (install with `ansible-galaxy install -r roles/requirements.yml

```yaml
---
- name: cjsteel.bootstrap
- name: cjsteel.parted
```

## Testing

### molecule testing and no_log debug option

You will need to set the environment variable of `MOLECULE_DEBUG` to log errors, alternately you may prefer to debug manually by using the  `--debug` flag. Here is an example applied against the *vagrant* molecule scenario:

```text
molecule --debug create -s vagrant
```



## License

Apache License, Version 2.0

## Author Information

[Christopher Steel](https://cjsteel.github.io/) <chris.steel@gmail.com>

This role was generated using a modified version of Robert de Bock's excellent ansible-role-skeleton

* [github.com/robertdebock/ansible-role-skeleton](https://github.com/robertdebock/ansible-role-skeleton)

See Robert's personal site for many examples of high quality Linux flavour and version agnostic roles. 

* [Robert de Bock](https://robertdebock.nl/)

Other collections of great public facing Ansible roles:

* [DebOps - Maciej Delmanowski](https://github.com/debops)
* [Jeff Geerling](https://github.com/geerlingguy)

* [Larry Smith Jr.](https://github.com/mrlesmithjr)

# ansible-role-parted
