GceInstance
===========

Setup VPC, firewall rules, etc. for single Google Cloud Environment (GCE) instance.

![Build status](https://travis-ci.org/jylitalo/GceInstance.svg?branch=master) 

Requirements
------------

Google Cloud Environment project and credentials.

Role Variables
--------------

* hostname: main
* machine_type: f1-micro
* open_ports: open smtp for localhost
* region: us-central1
* zone: us-central1-c
* open_ports:
  * {protocol: tcp, port: tcp:25, src: 127.0.0.1/32}

Dependencies
------------

None

Example Playbook
----------------

    - hosts: server
      roles:
         - { role: GceInstance, hostname: foobar }

License
-------

MIT

Author Information
------------------

Juha Ylitalo, juha.ylitalo@gmail.com, http://www.ylitalot.com/
