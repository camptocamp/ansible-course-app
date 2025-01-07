# App for the Ansible training course

This branch is for installing WordPress with separate roles that are stored in different git repositories/branches.

Install the role requirements

```shell
$ ansible-galaxy install -r requirements.yml
```

Run the playbook that calls the roles

```shell
$ ansible-playbook -i ip.ad.dr.ess, site.yml
```
