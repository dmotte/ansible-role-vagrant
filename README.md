# ansible-role-vagrant

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dmotte/ansible-role-vagrant/release?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-vagrant/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.vagrant-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/vagrant)

Ansible role to install **Vagrant** on Debian/Ubuntu hosts.

The installation steps were taken from: https://developer.hashicorp.com/vagrant/downloads.

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your _Ansible Playbook_ like this:

   ```yaml
   - name: Include the dmotte.vagrant role
     ansible.builtin.include_role: { name: dmotte.vagrant }
     vars: { ansible_become: true }
   ```

> **Note**: this role must be run as root (`ansible_become: true`).

## Development

If you want to contribute to this project, you can use the [`test/playbook.yml`](test/playbook.yml) file to test the role while editing it.

Place your inventory file (e.g. `hosts.yml`) inside the `test` folder.

You can then **execute the playbook** against your host:

```bash
cd test/
ansible-playbook -i hosts.yml playbook.yml
```
