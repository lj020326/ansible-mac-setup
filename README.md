# macOS Monterey setup using Ansible

<p float="left">
  <img src="./pics/macOS.jpeg" width="100" />
  <img src="./pics/ansible.png" width="80" /> 
</p>

This is my personal macOS config/setup using Ansible and will be updating it as I go along. (Currently compatible for macOS Monterey)

## How to install & Pre-reqs

I created a simple shell script in `scripts/prepare.sh` which will perform the initial steps of automating. This also installs pre-requisites like Ansible. 

Once pre-requisites are complete - you may install using ```scripts/apply.sh```. This runs ```ansible-playbook -i hosts -c local ansible_mac.yml --ask-become-pass``` in the background installing all the tools with Ansible. 

## What am I installing

- Main tools are located in ```ansible_mac.yml```

Tools to be installed:

- Zsh + Oh My Zsh as the primary shell
- Homebrew + all my default CLI tools (like kubectl, go CLI, awscli, azure CLI, trivy, terraform etc)
- Docker & Rancher Desktop
- VSCode + default plugins and configuration
- Asdf for version management: Golang, JS, Python

## For Customisation

Everything can be customised by editing `ansible_mac.yml`