# README.md

# Ansible Role: Group v1.0

An Ansible role that simply creates/removes groups

Occassionally, you will need to create groups between role executions, there is no built-in way to do this, instead use this role in between.

See Also: ansible-role-directory

![travis-ci](https://travis-ci.org/mm0/ansible-role-group.svg?branch=master)

## Requirements

None 

## Role Variables

Available variables are listed below, along with default values:

    the_groups: 
    - name: testgroup
      state: present # a list of groups to create/remove
    - name: testgroup
      state: absent # a list of groups to create/remove

## Dependencies

None 

## Example Playbook

    - hosts: webservers
      roles:
      - { role: ansible-role-group,
          the_groups: [{"name":"testgroup","state":"present"},{"name":"testgroup2","state":"absent"}]
        }

## License

MIT
