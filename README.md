# Ansible playbook for Raspberry Pi

Configures a fresh Raspberry Pi OS installation for me, using Ansible.

## Setup

```bash
python3 -m venv --upgrade-deps venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage

```bash
ansible-playbook main.yml
```
