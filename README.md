# Setup Ubuntu development environment

Ansible playbook to configure Windows Linux Subsystem v2 Ubuntu 20.04. It is not very elegant but it is functional.

## Prerequisites

The only prerequisites are : 

- Ubuntu 20.04 installed
- Ansible installed

> The commands to install Ansible are also available in a gist available here : [setup-ansible.sh](https://gist.github.com/pondichys/b4b7c1e17d22ae2d6f2d1c91611707f8)

## Running the playbook

Clone this repository.

Adapt the user variable if needed (or pass it through `--extra-vars` argument).

Run the playbook with `-K` option to supply the `sudo` password.

```bash
# Running on standard Ubuntu
ansible-playbook playbook-setup-ubuntudev.yml -K

# Running on WSL Ubuntu
 ansible-playbook -K playbook-setup-ubuntudev.yml --extra-vars "wsl_install=yes"
```

## Packages installed

The following packages are installed by this playbook:

- some base packages: git,curl,wget,python3-pip,python3-venv,apt-transport-https,ca-certificates,software-properties-common,bzip2
- [azure-cli](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest)
- aws-cli
- kubectl
- kind
- k9s
- helm
- restic
- [powerline go](https://github.com/justjanne/powerline-go)
