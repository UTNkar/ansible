# UTN Ansible

This repository contains the deployment scripts used by the UTN servers.
Playbooks are located in the root directory and are named after the various
applications they deploy. The exception to this rule is `common.yml` which
includes basics for all server machines, i.e. user management and firewall
setup.

## Contributing

Although this repository is mainly meant for the UTN system administrator it is
open to contributions and improvements.

## Example

To deploy the drupal 7 websites:

1. Make sure you've entered your vault password in `password.txt`
2. Make sure you've made a file for the selected host as shown in `host_vars/example.utn.se`.
3. Run `ansible-playbook drupal7.yml`
