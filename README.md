## WordPress+Nginx+PHP-FPM+MariaDB on Debian11 Deployment

- Requires Ansible 1.2 or newer
- Expects Debian 11 host/s

These playbooks deploy a simple all-in-one configuration of the popular
WordPress blogging platform and CMS, frontend by the Nginx web server and the PHP-FPM process manager. 
To use, copy the `hosts.example` file to `hosts` and edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml

The playbooks will configure MariaDB, WordPress, Nginx, and PHP-FPM on every single host defined as a wordpress-server. When the run
is complete, you can hit access server to begin the WordPress configuration.

If you need to clean the VM to restart a test from scratch, run :

	ansible-playbook -i hosts purge.yml

### Ideas for Improvement

These playbooks could be extended to separate the components (PHP-FPM, MySQL, Nginx) onto separate hosts and handle the configuration appropriately.