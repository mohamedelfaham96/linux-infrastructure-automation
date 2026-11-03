# Multi-Node Linux Infrastructure Automation Lab

A practical Linux system administration and infrastructure automation project built using Ansible, CentOS Stream 8, Oracle Cloud Infrastructure, Nginx, Firewalld, Fail2Ban, LVM, Bash, Cron, Git, Jinja2, and Ansible Vault.

## Project Overview

This project manages two Linux servers from a central Ansible Control Node.

- Control Node: `faham`
- Managed Node: `faham-node02`
- Operating System: CentOS Stream 8
- Cloud Platform: Oracle Cloud Infrastructure
- Automation Tool: Ansible Core
- Web Server: Nginx
- Firewall: Firewalld
- Intrusion Protection: Fail2Ban
- Version Control: Git

## Architecture

```text
                         Oracle Cloud Infrastructure
                                    |
                         Virtual Cloud Network
                                    |
                +-------------------+-------------------+
                |                                       |
        Ansible Control Node                      Managed Node
              faham                              faham-node02
           10.0.0.83                               10.0.0.5
                |                                       |
                +---------- SSH Key Authentication -----+
                                    |
                         Centralized Automation
