# ansible-nextcloud-ubuntu
Deploy Nextcloud on Ubuntu 16.04 using nginx, php-fpm, postgresql

1. Edit hosts file and enter your IP address for the nc01 node.
2. Run the nc01-bootstrap.yml playbook in order to install python2 (needed for ansible).
3. Edit the group_vars/all/nextcloud.yml, make sure to set proper values for passwordsalt, secret and instanceid (e.g. from a previous/manual nextcloud installation).
4. Edit the group_vars/all/postgres.yml, these are the passwords for the postgresql users.
5. Ideally you should re-create the postgres.yml and nextcloud.yml group_vars files as `Ansible Vaults` so that the values are encrypted. The provided plain-text versions are just a guideline.
6. Adjust the nc01.yml playbook as you want, edit the roles/tasks/templates if needed.
7. Run the nc01.yml playbook
8. Done.


## Disclaimer
Use at your own risk! I am not responsible for any data loss or other problems when you use code from this repository.
Also this repository ships the code *as is* and I am neither giving any support nor promising active maintenance of this repo.
