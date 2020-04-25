# Role Name: DOTNET-CORE

[![Build Status](https://travis-ci.org/deluxebrain/ansible-role-dotnet-core.svg?branch=master)](https://travis-ci.org/deluxebrain/ansible-role-dotnet-core)

.Net Core installer for Linux.

## Requirements

None.

## Role Variables

All of the listed variables are defined in `defaults/main.yml`.
Individual variables can be set or overridden by setting them in a playbook for this role.

- `dotnetcore_version: 3.0`: ( default: latest )
  - .Net Core version to install

## Dependencies

None.

## Example Playbook

Example below for the following:

- Installation of specific versions of .Net Core

```yaml
- hosts: servers
  roles:
      - deluxebrain.dotnet-core
        dotnetcore_version: 3.1
```

## Development Installation

The included files, `requirements-dev.txt` and `requirements.txt` install development and production dependencies accordingly.

The included Makefile includes several targets related to the installation of the development environment and the management of the development process.

Packages are managed through the `pip-tools` suite. This, and other development requirements, are installed through the `requirements-dev.txt` file.

```sh
# Create project virtual environment
# Install development dependencies into virtual environment
make install
```

`pip-tools` manages the project dependencies through the included `requirements.in` file, and is responsible both for the generation of the `requirements.txt` file and package installion into the virtual environment.

Note that this means that the `requirements.txt` file *should not be manually edited* and must be regenerated every time the `requirements.in` file is changed.

```sh
# Compile the requirements.in file to requirements.txt
# Install the requirements.txt pacakges into the virtual environment
make sync
```

## License

MIT / BSD

## Author Information

This role was created in 2020 by [deluxebrain](https://www.deluxebrain.com/).
