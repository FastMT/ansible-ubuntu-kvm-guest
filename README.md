# ansible-ubuntu-kvm-guest
Ansible role to configure KVM linux (Ubuntu) guest 

## Description

Role performs KVM guest agent installation and configuration:
 - Install KVM guest agent
 - If /dev/vda1 partition is less than 2Gb it's extend it

## Installation

Create requirements.yml file

```
# Include ubuntu-kvm-guest role
- src: https://github.com/FastMT/ansible-ubuntu-kvm-guest.git
  name: ubuntu-kvm-guest
  version: "v1.0.0"
```

Install external module into ~/.ansible/roles folder

```
ansible-galaxy install -r requirements.yml
```

## Usage

playbook.yml:

```
# Configure KVM Guest
- role: "ubuntu-kvm-guest"
```        