This task deploy two virtual machines for run WordPress.
Short description roles:
- apache2 - install web server
- db - install and configure database server
- users - create system account
- wp - install necessary packages and download and configure wordpress

For using you only need run `vagrant up` and after some time go to http://192.168.33.10/


What else needs to be done:
- protect site by LDAP
- create group_vars for roles db and users( need for create users)
