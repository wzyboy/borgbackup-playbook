# BorgBackup Ansible Playbook

A simple Ansible Playbook to install and set up [BorgBackup](https://borgbackup.readthedocs.io/en/stable/).

- You need `borg init` the target repository first;
- If using rsync.net as backup host, public key could be automatically installed by passing `-e borg_setup_pubkey=True`.
