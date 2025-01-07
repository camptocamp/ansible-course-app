[![ansible-lint](https://github.com/camptocamp/ansible-course-app/actions/workflows/ansible-lint.yml/badge.svg?branch=molecule)](https://github.com/camptocamp/ansible-course-app/actions/workflows/ansible-lint.yml)

# App for the Ansible training course

This branch is for installing WordPress with separate roles that are stored in different folders.

Also it includes molecule for testing during the role development.

Setup molecule

```shell
$ python3 -m venv .venv
$ source .venv/bin/activate
$ python3 -m pip install -r requirements.txt
```

Run molecule tests

```shell
$ cd roles/molecule_tests
$ molecule test
```

Run the playbook that calls the roles

```shell
$ ansible-playbook -i ip.ad.dr.ess, site.yml
```
