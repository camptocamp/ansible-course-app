[![ansible-lint](https://github.com/camptocamp/ansible-course-app/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/camptocamp/ansible-course-app/actions/workflows/ansible-lint.yml)

# App for the Ansible training course

The repository content is spread across different branches.

They all aim to install WordPress with Ansible.

* master

  This branch includes a README.md to help you navigate this repository.

* single-role

  Includes a one-size-fits-all role.

* multi-role

  Includes several roles that each serve distinct purposes, eg. to setup MariaDB or nginx.

  With molecule it has a way of advanced containerized testing during role development.

* role-per-repo

  Includes role `requirements.yml` and a playbook `site.yml` to instantiate it.
  
  The `requirements.yml` imports the following roles that are spread across these branches (also in this repository):
    * common
    * mariadb
    * nginx
    * php-fpm
    * wordpress
