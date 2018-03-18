Role Name
=========

Docker registry installation

Requirements
------------

No requirements

Role Variables
--------------

Mandatory variables:
* dockerRegistrySslKey
* dockerRegistrySslCertificate

Optional variables:
* dockerRegistryPort (default: 5000)
* dockerRegistryStorageLocation (default: /var/lib/registry)

Dependencies
------------

* dockerce.install

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - dockerce.install
         - dockerce.registry

License
-------

BSD
