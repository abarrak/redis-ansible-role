Redis Ansible Role
=========

A redis ansible role based on [Bitnami's chart](https://github.com/bitnami/charts/tree/master/bitnami/redis).

Requirements
------------

A one of kubernetes cluster nodes as host target to run against.

Role Variables
--------------

The default varibales are defined in `defaults/main.yml` and `vars/main.yml`, such as chart versions and should be overriden as convenient. All the [chart variables](https://github.com/bitnami/charts/blob/master/bitnami/redis/values.yaml) can be set there as well.

Dependencies
------------

A requirement of `helm` role is specified  as `./requirements.yml`

Usage
-----

1. Install the requirements, then include the role in your playbook as follows:

  ```yaml
  ansible-galaxy -r requirements.yml
  ```

2. Specify your preferences, (e.g. redis chart version, helm version, etc.) if needed.

3. Include the role into your playbook, then run it.

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
