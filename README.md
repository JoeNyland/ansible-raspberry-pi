# Ansible playbook for Raspberry Pi

Configures a Raspberry Pi OS installation for me, using Ansible.

## Usage

### Fresh Raspberry Pi OS installation

On a fresh installation, only password authentication is available. However, by default, Ansible wants to use `sshpass`, which is not available on macOS.

Instead, we tell Ansible to use `paramiko` for the connection, which is installed in the setup section [above](#Setup).

The default password is 'raspberry'. This is just the default password and it will be removed in the playbook.

```bash
ansible-playbook --connection=paramiko --ask-pass playbooks/main.yml
```

### Existing Raspberry Pi OS installation

Once the Raspberry Pi has been configured [above](#fresh-raspberry-pi-os-installation), SSH keys can now be used for authentication and we no longer need to override the connection provider or provide a password.

```bash
ansible-playbook playbooks/main.yml
```
