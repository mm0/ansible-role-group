Ansible Role: Group v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-group.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-group)


An Ansible role that simply creates/removes groups

Occassionally, you will need to create groups between role executions, there is no built-in way to do this, instead use this role in between.

See Also: ansible-role-user


Requirements
---

None 

Role Variables
---

Available variables are listed below, along with default values:

```yml
the_groups: 
- name: testgroup
  state: present # a list of groups to create/remove
- name: testgroup
  state: absent # a list of groups to create/remove
```

Dependencies
---

None 

Example Playbook
---

```yml
- hosts: webservers
  roles:
  - { role: ansible-role-group,
      the_groups: [{"name":"testgroup","state":"present"},{"name":"testgroup2","state":"absent"}]
    }
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github