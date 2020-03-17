# UTN Ansible

This repository contains the deployment scripts used by the UTN servers.
Playbooks are located in the root directory and are named after the various
applications they deploy. The exception to this rule is `common.yml` which
includes basics for all server machines, i.e. user management and firewall
setup.

## Installations and instructions

1. Install [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).
1. Clone this repository
1. Install dependencies by running `ansible-galaxy install -r ansible-requirements.yml`
1. Create a file called password.txt that contains the vault password
1. In the folder host_vars, create a file for each of the servers, named according to the FQDN of the server (e.g., turing.utn.se), containing your sudo password for that host.

You should now be able to run all playbooks in the repository using ansible-playbook [playbook].
All instructions and description of all playbooks can be found on <https://docs.utn.se/development_tools/ansible/>

## Troubleshooting

If you are getting an error saying ansible is being run in a world writable directory, you need to change the permissions on the ansible folder. Go to your ansible directory `cd /path/to/ansible` and execute `chmod 775 .`.

## Contributing

Although this repository is mainly meant for the UTN system administrator it is
open to contributions and improvements.
