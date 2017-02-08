# Ansible Role - Powerline

[![Ansible Role](https://img.shields.io/ansible/role/15428.svg)](https://galaxy.ansible.com/nass600/powerline/)
[![Build Status](https://travis-ci.org/nass600/ansible-role-powerline.svg?branch=master)](https://travis-ci.org/nass600/ansible-role-powerline)

Installs and configures [Powerline](http://powerline.readthedocs.io/en/master/index.html) in Linux and macOS systems.

## Requirements

This role assumes you have the config files already located in your filesystem (i.e colorschemas, themes...).

## Role Variables


Available variables are listed below, along with default values (see `defaults/main.yml`):

#### powerline


    powerline_package_name: "powerline-status"

Powerline package name to install. You can add a custom version if you need to.


    powerline_version: ""

Powerline version to install. Default: empty meaning latest.


    powerline_extra_segments:
      - { name: powerline-gitstatus, version: "v1.2.1"}

Additional powerline [segments](http://powerline.readthedocs.io/en/master/configuration/segments.html) that should be installed.

    powerline_daemon_destination: "~/.bashrc"

File where you want to set the powerline daemon launch

#### powerline config

    powerline_config_dir: "~/.config/powerline"

Location of the powerline config files. This directory is where the main `config.json` is going to be created.


    powerline_config_shell_colorscheme: "default"
    powerline_config_shell_theme: "default"
    powerline_config_vim_colorscheme: "default"
    powerline_config_vim_theme: "default"

Themes used for generating the `config.json`.


#### powerline fonts

    powerline_fonts_repo: "git://github.com/powerline/fonts.git"

Repository where the patched fonts are located.

    powerline_fonts_dir: "{{ powerline_config_dir }}/fonts"

Directory where you want to place the downloaded fonts.


## Dependencies

+ Python + Pip

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: nass600.powerline }


## License

[MIT](/src/master/LICENSE)


## Author Information

Ignacio Velazquez Gomez - [http://ignaciovelazquez.es]()
