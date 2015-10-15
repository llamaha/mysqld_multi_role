# mysqld_multi_role
Ansible Role for configuring stand-alone MariaDB instances on Centos 7


This role is in development and needs to be tested before pushing to ansible-galaxy.  Pull requests are welcome!

Once finished this role will complete the following tasks:
1. Verify MariaDB installation.
2. Create a new MariaDB datadir in the location specified either in defaults or a custom playbook.
3. Calculate the number of current standalone databases to ensure position of deployment.
4. Add a new configuration to /etc/my.cnf.d under name of application specified either in defaults or custom playbook.  A new port number will be allocated automatically.
5. Create a systemd service under /etc/systemd/system/mariadb-app_name.service to be controlled by systemctl.
6. Start the database service with custom log, socket and pid locations.
