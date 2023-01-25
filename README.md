# ansible-role-bloodhound #

## ⚠ Notice ⚠ ##

This project has been archived, as this Ansible role is not currently
being used.  It was used in
[cisagov/kali-packer](https://github.com/cisagov/kali-packer), but the
assessors asked for the most recent version of Bloodhound from GitHub
to be installed instead.  If this Ansible role is ever put into
service again, it can be unarchived.

[![GitHub Build Status](https://github.com/cisagov/ansible-role-bloodhound/workflows/build/badge.svg)](https://github.com/cisagov/ansible-role-bloodhound/actions)
[![CodeQL](https://github.com/cisagov/ansible-role-bloodhound/workflows/CodeQL/badge.svg)](https://github.com/cisagov/ansible-role-bloodhound/actions/workflows/codeql-analysis.yml)

This is an ansible role for installing
[BloodHound](https://github.com/BloodHoundAD/BloodHound).

## Requirements ##

None.

## Role Variables ##

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| password | The password used for `neo4j`. | Random password created with the [Ansible password module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/password_lookup.html). | No |

## Dependencies ##

None.

## Example Playbook ##

Here's how to use it in a playbook:

```yaml
- hosts: all
  become: yes
  become_method: sudo
  tasks:
    - name: Install BloodHound
      ansible.builtin.include_role:
        name: bloodhound
```

## Contributing ##

We welcome contributions!  Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for
details.

## License ##

This project is in the worldwide [public domain](LICENSE).

This project is in the public domain within the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain
dedication](https://creativecommons.org/publicdomain/zero/1.0/).

All contributions to this project will be released under the CC0
dedication. By submitting a pull request, you are agreeing to comply
with this waiver of copyright interest.

## Author Information ##

Kyle Evers - kyle.evers@trio.dhs.gov
