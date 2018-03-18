Role Name
=========

Role to install Docker CE on CentOS 7

Requirements
------------

No requirements

Role Variables
--------------

* dockerTrustRegistry (default: optional)
* dockerClientCACertificat
* dockerClientPrivateKey

Dependencies
------------

No dependencies

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: dockerce.install
           dockerTrustRegistry:
             domain: registrydomain
             certificate: <certificat>

License
-------

BSD
