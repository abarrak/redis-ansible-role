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

Install the requirements, then include the role in your playbook as follows:

```yaml
ansible-galaxy -r requirements.yml
```

License
-------

MIT.

Author Information
------------------

Abdullah Barrak [(@abarrak)](https://github.com/abarrak).
