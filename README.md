![Ansible Lint](https://github.com/johanneskastl/ansible-role-personal_workstation_setup/workflows/Ansible%20Lint/badge.svg)

# personal_workstation_setup

Ansible role to set up my personal workstation (with openSUSE Tumbleweed,
openSUSE MicroOS or Fedora Kinoite)

## Requirements

None.

## Role Variables

- `additional_flatpak_packages` (List of Strings): List of Flatpaks to install,
  in addition to the ones in `flatpak_packages` that this role sets (see below)

### Optional variables

- `flatpak_packages` (List of Strings): List of Flatpaks to install
- `flathub_repository` (String): Flathub repository to use
  (default: `https://flathub.org/repo/flathub.flatpakrepo`)
- `flathub_system` (Boolean): Whether to use a `user`-scope or `system`-scope
  flatpak repository (default: `false`, i.e. `user`-scope)

### Optional variables for openSUSE

- `distribution_packages_to_remove` (List of Strings): RPM packages to be
  uninstalled
- `distribution_packages` (List of Strings): RPM packages to be installed
- `additional_distribution_packages` (List of Strings): variable to specify
  additional packages to install

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: johanneskastl.personal_workstation_setup
```

## License

BSD-3-Clause

## Author Information

I am Johannes Kastl, reachable via git@johannes-kastl.de
