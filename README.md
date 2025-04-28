# Yii2 PHP Application Deployment - DevOps Project

## Overview
Deploy a Yii2 app with Docker Swarm, NGINX, CI/CD using GitHub Actions, and Infrastructure Automation using Ansible.

## Setup Instructions

### 1. Infrastructure
- Launch a Ubuntu EC2 instance.
- SSH into it and allow ports 22, 80, and 8080.

### 2. Ansible
- Configure `ansible/hosts` with your EC2 details.
- Run:
  ```bash
  ansible-playbook -i ansible/hosts ansible/playbook.yml
