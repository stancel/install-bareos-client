install-bareos-client
=========

A role to install the bareos client onto an Ubuntu machine and open up the required firewall ports (9102) so that it can communicate with the bareos-director server component.

Requirements
------------

None. Well, you'll want to already be using Bareos or Bacula if you are using this role.

Role Variables
--------------

The bareos client's password 

```
	install_bareos_client_client_password: "Some very long string password here (47 characters)"
```
Which (numerical) version of Ubuntu you are installing this onto (default = 18.04)

```
	install_bareos_client_bareos_ubuntu_install_version: "18.04"
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
	- hosts: your_server
	  vars_files:
	    - vars/main.yml
	  roles:
	    - { role: stancel.install-bareos-client }
```

or 

```
	- hosts: your_server 
	  vars:
		install_bareos_client_client_password: "Some very long string password here"
		install_bareos_client_bareos_ubuntu_install_version: "16.04"
	  roles:
	    - { role: stancel.install-bareos-client }
```

License
-------

GPLv3

Author Information
------------------

[Brad Stancel](https://github.com/stancel)