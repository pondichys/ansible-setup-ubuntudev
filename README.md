# Setup Ubuntu development environment - STIB-MIVB DCP laptop

Ansible playbook to configure a Ubuntu workstation for my job as DCP engineer. 

This playbook is minimalistic as most of the tools we use for our day-to-day job are packaged in a container image that we use in conjunction with Distrobox.
This allows us to be sure that everyone is working with the same version of the tools.

## Prerequisites

- Ubuntu >= 22.04 installed
- Ansible installed

> The commands to install Ansible are also available in a gist available here : [setup-ansible.sh](https://gist.github.com/pondichys/b4b7c1e17d22ae2d6f2d1c91611707f8)

## Running the playbook

Clone this repository.

Run the playbook with `-K` option to supply the `sudo` password.

```bash
# Running on standard Ubuntu
ansible-playbook playbook-setup-ubuntudev.yml -K
```
