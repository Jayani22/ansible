# Ansible Automation Practice

This repository contains my hands-on practice with **Ansible**, focusing on automating infrastructure configuration, application deployment, and system management tasks.

It is part of my DevOps learning journey to build real-world automation skills using Infrastructure as Code (IaC).

---

## Project Overview

This project demonstrates how to use Ansible for:

- Configuration Management
- Application Deployment
- Task Automation across multiple servers

Ansible works in an **agentless architecture**, connecting to remote machines via SSH and executing tasks defined in YAML-based playbooks.

---

## Tech Stack

- Ansible
- Linux
- YAML (Playbooks)
- SSH
- Git & GitHub
---

## Key Concepts Covered

- Ansible Installation & Setup
- Inventory Management
- Ad-hoc Commands
- Playbooks (YAML)
- Roles & Reusability
- Variables & Templates
- SSH-based Automation

---

## Setup & Usage

### Install Ansible

```bash
sudo apt update
sudo apt install ansible -y
```

---

### Configure Inventory

Edit the hosts file:

```bash
sudo nano /etc/ansible/hosts
```

Example:

```ini
[web]
192.168.1.10

[db]
192.168.1.20
```

---

### Test Connection

```bash
ansible all -m ping
```

---

### Run a Playbook

```bash
ansible-playbook playbooks/sample.yml
```

---

## Example Playbook

```yaml
---
- name: Install Nginx
  hosts: web
  become: yes

  tasks:
    - name: Install package
      apt:
        name: nginx
        state: present
```

---

## Key Features

- Agentless automation using SSH
- Simple YAML-based configuration
- Reusable roles for modular design
- Scalable automation across multiple servers

---

## Learning Outcomes

Through this repository, I gained:

- Practical experience in automation using Ansible
- Understanding of Infrastructure as Code
- Ability to manage multiple servers efficiently
- Skills in writing reusable and scalable playbooks

---

## Future Enhancements

- Integrate with Docker & Kubernetes
- Add CI/CD pipeline using GitHub Actions
- Deploy infrastructure on AWS using Ansible
- Implement Ansible Tower / AWX

---

## Note

This repository is created for learning and practicing Ansible concepts used in real-world DevOps environments.
