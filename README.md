# Monitoring & Logging Stack

This repository contains a comprehensive DevOps stack for monitoring, utilizing tools such as Prometheus, Grafana, Blackbox Exporter, Alertmanager, and Process Exporter. The stack is configured for deployment using Ansible.

## Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
- [Ansible Setup](#ansible-setup)
- [Running Ansible Playbooks](#running-ansible-playbooks)

## Overview

This repository is organized to deploy a complete monitoring solution. It includes configurations and deployment scripts for various components, leveraging Ansible for configuration management.

## Folder Structure

```sh
├── ansible
│   └── roles
│       ├── alertmanager
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   ├── default
│       │   │   │   └── tests
│       │   │   └── latest
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       ├── blackbox_exporter
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   ├── default
│       │   │   │   └── tests
│       │   │   └── latest
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       ├── grafana
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   └── default
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       │       └── distro
│       ├── nginx
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   └── default
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       ├── node_exporter
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   ├── default
│       │   │   │   └── tests
│       │   │   └── latest
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       ├── process_exporter
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   ├── default
│       │   │   │   └── tests
│       │   │   └── latest
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       ├── prometheus
│       │   ├── defaults
│       │   ├── handlers
│       │   ├── meta
│       │   ├── molecule
│       │   │   ├── agentmode
│       │   │   │   └── tests
│       │   │   ├── alternative
│       │   │   │   └── tests
│       │   │   ├── default
│       │   │   │   └── tests
│       │   │   └── latest
│       │   │       └── tests
│       │   ├── tasks
│       │   ├── templates
│       │   └── vars
│       └── users
│           ├── defaults
│           └── tasks
└── variables
    └── ansible
        ├── env
        │   ├── common.yml
        │   ├── custom-alertrules
        │   │   ├── blackbox_exporter_alerts.rules
        │   │   └── node_exporter_alerts.rules
        │   ├── custom-dashboards
        │   │   ├── alert123.json
        │   │   ├── custom3.json
        │   │   └── process.json
        │   └── nginx.yml
        └── hosts

