andrewrothstein.pki
=========
![Build Status](https://github.com/andrewrothstein/ansible-pki/actions/workflows/build.yml/badge.svg)

A role for managing a PKI. Leverags cfssl to build a CA key/cert, and collection of key/cert
pairs for a fleet of hosts. Supports subject alternate names. Saved me from having to
learn the openssl command line!

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

Recommended to target localhost if you're managing a local eyes-above-the-wall PKI.

```yml
- hosts: localhost
  connection: local
  roles:
    - role: andrewrothstein.pki
	  pki_dir: ~/pki
      pki_self_sign: Ture
	  pki_ca:
	    cname: ca.foo.io
	  pki_servers:
	    - cname: host1.foo.io
		- cname: host2.foo.io
		- cname: host3.foo.io
```

License
-------

MIT

Author Information
------------------

Andrew Rothstein <andrew.rothstein@gmail.com>
