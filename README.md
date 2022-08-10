Redis Ansible Role
=========

A redis ansible role based on [Bitnami's chart](https://github.com/bitnami/charts/tree/master/bitnami/redis).

Requirements
------------

A one of kubernetes cluster nodes as host target to run against, or control node with linked `kubeconfig`.

Role Variables
--------------

The default varibales are defined in `defaults/main.yml`, (e.g. versions) and should be overriden as convenient.

All the [helm chart variables](https://github.com/bitnami/charts/blob/master/bitnami/redis/values.yaml) can be set there as well.

Dependencies
------------

A requirement of `helm` role is loaded with the role's Dependencies automatically.

Usage
-----

Install the requirements, then include the role in your playbook as follows:

```yaml
ansible-galaxy install abarrak.redis_ansible_role
```

```yaml
- hosts: all
  roles:
    - role: redis-ansible-role
```

To uninstall, include the relative tasks from role:

```yaml
- name: uninstall redis
  ansible.builtin.include_role:
    name: redis-ansible-role
    tasks_from: 'uninstall'
```

License
-------

MIT.

Author Information
------------------

Abdullah Barrak [(@abarrak)](https://github.com/abarrak).
