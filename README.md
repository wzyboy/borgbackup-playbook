# BorgBackup Ansible Playbook

A simple Ansible Playbook to install and set up [BorgBackup](https://borgbackup.readthedocs.io/en/stable/).

## Requirements

- You need `borg init` the target repository first;
- If passing `-e borg_setup_pubkey=True`, a pair of SSH key would be generated on the host to be backed up (if not existed), and installed to the backup host;
- If using rsync.net as backup host, special tasks would be run to ensure the installation of the public key.

## Usage

1. Copy `hosts.example` to `hosts` and edit it properly.
2. Optionally edit the vars in `site.yaml`. They can be overridden by `-e key=value`.
3. Run `ansible-playbook -i hosts site.yaml`.
