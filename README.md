# Homelab Ansible

Ansible project for automating and managing my personal homelab.

The main goal is to learn Infrastructure as Code and practical DevOps skills by managing real Linux servers instead of configuring them manually.

## Current infrastructure

- `docker-vm` - Ubuntu Server, Docker host
- `erp-vm` - Ubuntu Server, Docker host
- Fedora workstation - Ansible control node

## Technologies

- Linux
- Ansible
- Docker
- SSH
- Tailscale
- Ansible Vault
- Git

## Project structure

```text
homelab-ansible/
├── inventory/
├── playbooks/
├── roles/
│   ├── common/
│   ├── update/
│   └── docker/
├── ansible.cfg
└── README.md
```

## Current features

- Linux system updates
- Support for Debian/Ubuntu and Red Hat based systems
- Common system configuration
- Docker installation and configuration
- Docker repository configuration
- Docker service management
- Adding users to the Docker group
- Ansible Vault for sensitive variables

## Usage

Run the main playbook:

```bash
ansible-playbook playbooks/bootstrap.yml
```

For Vault-protected variables:

```bash
ansible-playbook playbooks/bootstrap.yml --ask-vault-pass
```

The project is designed to be idempotent, so running the playbook multiple times should not make unnecessary changes.

## Roadmap

- [ ] Docker Compose deployments
- [ ] Nginx
- [ ] AdGuard Home
- [ ] Prometheus & Grafana
- [ ] Automated backups
- [ ] GitHub Actions
- [ ] More services and Ansible roles

**Status:** Work in progress
