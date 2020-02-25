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

## License

MIT / BSD

## Author Information

This role was created in 2020 by [deluxebrain](https://www.deluxebrain.com/).
