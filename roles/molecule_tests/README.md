Role Name
=========

This role is designed to test the installation of a Wordpress server on a Debian 11 hosts (variants normal and slim)

Requirements
------------

This relies on a working installation of a Rootless podman setup.
Basically, if you can do a `podman pull alpine` succesfully, you should be able to run the tests 

Role Variables
--------------

The following variables should be defined in the `vars/main.yml` file:
```
# Version of wordpress to install
wp_version

# These are the WordPress database settings
wp_db_name
wp_db_user
wp_db_password

# This is used for the nginx server configuration, but access to the
# WordPress site is not restricted by a named host.
server_hostname

# Disable All Updates
# By default automatic updates are enabled, set this value to true to disable all automatic updates
auto_up_disable

# Define Core Update Level
# true  = Development, minor, and major updates are all enabled
# false = Development, minor, and major updates are all disabled
# minor = Minor updates are enabled, development, and major updates are disabled
core_update_level
```

Dependencies
------------

None

Example : How to run molecule tests
----------------

```
export PY_COLORS=1; export ANSIBLE_FORCE_COLOR=1;
cd roles/molecule_tests
molecule test
```
