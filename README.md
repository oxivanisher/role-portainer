portainer
=========
[![Ansible Lint](https://github.com/oxivanisher/role-portainer/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-portainer/actions/workflows/ansible-lint.yml)

This role installs and configures portainer.
It will also install a systemd timer that cleans portainer resources.

Role Variables
--------------

| Name                        | Comment                                                 | Default value    |
|-----------------------------|---------------------------------------------------------|------------------|
| portainer_ip                | On which IP will portainer listen on                    | `0.0.0.0`        |
| portainer_prune_olderthan   | Prune resources only if they are older than             | `744h` (31 days) |
| portainer_docker_compose_v2 | Use docker compose v2 (required for i.e. Ubuntu 24.04!) | `false`          |

Example Playbook
----------------
```yaml
- name: Install portainer
  hosts: docker_hosts
  roles:
    - role: oxivanisher.linux_server.portainer
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_server](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_server/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_server).
