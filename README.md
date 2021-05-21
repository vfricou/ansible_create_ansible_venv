# Ansible create virtual venv

This playbook is written to fully automaticaly create ansible virtual-env for multiples ansible versions.  

All virtualenv whas made with python3 and include :
- ansible
- netaddr
- ansible-autodoc
- ansible-lint
- yamllint
- flake8
- molecule
- molecule-docker
- molecule-podman

All theses packages was installed by `pip install` managed through ansible.

The virtualenv created by this playbook are set from `ansible_version` variable :

## Variable Customization

| Name                   | Default                               | Description                      |
| ---------------------- | ------------------------------------- | -------------------------------- |
| base_venv_path         | `'${HOME}/venv/ansible'`              | Path to store ansible virtualenv |
| base_requirements_path | `'${HOME}/venv/ansible/requirements'` | Path to find requirements files  |
| ansible_versions       | `['2.8', '2.9', '2.10', 'latest' ]`   | Ansible versions to install      |