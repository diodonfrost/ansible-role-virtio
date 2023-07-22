# ansible-role-virtio

[![molecule](https://github.com/diodonfrost/ansible-role-virtio/workflows/molecule/badge.svg)](https://github.com/diodonfrost/ansible-role-virtio/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-diodonfrost.virtio-660198.svg)](https://galaxy.ansible.com/diodonfrost/virtio)

This role provide a compliance for install Virtio drivers on your target host.

## Requirements

None.

## Role Variables

This role has multiple variables. The defaults for all these variables are the following:

```yaml
---
# defaults file for diodonfrost.virtio

# URL to download virtio iso
virtio_iso_url: "{{ _virtio_iso_url }}"

# Update virtio if it is already installed
virtio_update: false
```

## Dependencies

None

## Example Playbook

This is a sample playbook file for deploying the Ansible Galaxy virtio role in a localhost and installing the latest version of virtio.

```yaml
---
- hosts: localhost
  become: true
  roles:
    - role: diodonfrost.virtio
```

## Local Testing

This project uses [Molecule](http://molecule.readthedocs.io/) to aid in the
development and testing.

To develop or test you'll need to have installed the following:

* Linux (e.g. [Ubuntu](http://www.ubuntu.com/))
* [Python](https://www.python.org/) (including python-pip)
* [Ansible](https://www.ansible.com/)
* [Molecule](http://molecule.readthedocs.io/)
* [Libvirt](hhttps://libvirt.org/)
* [Vagrant](https://www.vagrantup.com/downloads.html)

### Testing with Libvirt

```shell
# Install requirements
pip install -r requirements-dev.txt

# Test ansible role on Windows
molecule test -s windows

# Create Windows virtual machine
molecule create -s windows

# Apply role on Window
molecule converge -s windows

# Launch tests on Windows
molecule verify -s windows
```

## License

Apache 2

## Author Information

This role was created in 2023 by diodonfrost.
