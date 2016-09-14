Ansible Role: Glassfish/Payara Server
=========

This role installs and configures the Glassfish/Payara server with admin and password for domain1 and makes available the asadmin tool throught the path for the specified user account. It installs the mysql connector also.

Requirements
------------

You need a __JDK8+__ installed on the system before run this role.

Role Variables
--------------

- __glassfish_user__: user on the system to put asadmin tool into .bashrc. Please change this.
- __glassfish_version__: version of the product (Payara), _4.1.1.163_ by default.
- __glassfish_install_dir__: /opt/glassfish by default
- __admin_password__: _admin_ by default
- __mysql_connectorj_version__: The mysql driver version to download. _5.1.39_ by default

Dependencies
------------

JDK8+ needed before run. Check for java galaxy roles like: _mrlesmithjr.oracle-java8_

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

			- hosts: all
			  vars:
			   - glassfish_user: "my-user-account"
			  roles:
				- ansible-role-glassfish

License
-------

MIT / BSD

Author Information
------------------

This role was created by David Palomar
