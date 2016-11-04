andrewrothstein.pki
=========

A role for managing a PKI. Leverags cfssl to build a CA key/cert, and collection of key/cert
pairs for a fleet of hosts. Supports subject alternate names. Saved me from having to
learn the openssl command line!

Requirements
------------

See (meta/main.yml)[meta/main.yml]

Role Variables
--------------

See (defaults/main.yml)[defaults/main.yml]

Dependencies
------------

See (meta/main.yml)[meta/main.yml]

Example Playbook
----------------

Recommended to target localhost if you're managing a local eyes-above-the-wall PKI.

    - hosts: localhost
      connection: local
      roles:
         - role: andrewrothstein.pki
	   pki_dir: ~/pki
	   ...see (defaults/main.yml)[defaults/main.yml]....

License
-------

MIT

Author Information
------------------

Andrew Rothstein andrew.rothstein@gmail.com
