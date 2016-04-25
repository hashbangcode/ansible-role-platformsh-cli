# Ansible Role: Platform.sh CLI

An Ansible role that installs the [Platform.sh CLI](https://github.com/platformsh/platformsh-cli).


## Requirements

- Linux or OS X
- PHP 5.5.9 or higher, with cURL support
- Git


## Role Variables

Available variables are listed below, along with their default values (see defaults/main.yml):

    platformsh_cli_version: v3.0.7

The version of the Platform.sh CLI to install. This seems to always have a preceding "v". See the [releases page](https://github.com/platformsh/platformsh-cli/releases) for more info.

    platformsh_cli_install_path: /usr/local/bin

The path where the Platform.sh CLI will be installed and available to your system. This should be in your user's $PATH so that you can run commands simply with `platform` instead of the full path.

    platformsh_cli_mode: 0775

The permissions to apply to the `platform` binary once installed.


## Dependencies

None.


## Example Playbook

```
- hosts: servers
  roles:
     - { role: hashbangcode.ansible-role-platformsh-cli }
```


## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) originally for use with [Vlad](https://github.com/hashbangcode/vlad).
