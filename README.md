# [Ansible role drush](#ansible-role-drush)

Install Drupal shell.

|GitHub|Issues|Pull Requests|Version|Downloads|
|------|------|-------------|-------|---------|
|[![github](https://github.com/buluma/ansible-role-drush/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-drush/actions/workflows/molecule.yml)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-drush.svg)](https://github.com/buluma/ansible-role-drush/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-drush.svg)](https://github.com/buluma/ansible-role-drush/pulls/)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-drush.svg)](https://github.com/buluma/ansible-role-drush/releases/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/drush)](https://galaxy.ansible.com/ui/standalone/roles/buluma/drush/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-drush/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- hosts: all
  name: Converge
  tasks:
    - ansible.builtin.include_role:
        name: buluma.drush
      name: Include buluma.drush
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-drush/blob/master/molecule/default/prepare.yml):

```yaml
---
- become: true
  gather_facts: false
  hosts: all
  name: prepare
  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-drush/blob/master/defaults/main.yml):

```yaml
---
drush_clone_depth: 1
drush_composer_cli_options: --prefer-dist --no-interaction
drush_composer_global_bin_path: ~/.config/composer/vendor/bin
drush_composer_global_install: false
drush_composer_path: /usr/local/bin/drush
drush_composer_update: false
drush_composer_version: ~9.0
drush_force_composer_install: false
drush_force_update: false
drush_install_from_source: false
drush_keep_updated: false
drush_launcher_install: true
drush_launcher_path: /usr/local/bin/drush
drush_launcher_phar_url: "https://github.com/drush-ops/drush-launcher/releases/download/{{ drush_launcher_version }}/drush.phar"
drush_launcher_version: "0.6.0"
drush_source_install_bin_path: /usr/local/bin/drush
drush_source_install_path: /usr/local/share/drush
drush_source_install_version: "8.x"
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-drush/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub |
|-------------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|

## [Context](#context)

This role is part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-drush/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|[Fedora](https://hub.docker.com/r/robertdebock/fedora)|all|
|[Ubuntu](https://hub.docker.com/r/robertdebock/ubuntu)|all|

The minimum version of Ansible required is 2.10, tests have been done on:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them on [GitHub](https://github.com/buluma/ansible-role-drush/issues).

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-drush/blob/master/LICENSE).

## [Author Information](#author-information)

[Michael Buluma](https://buluma.github.io/)

