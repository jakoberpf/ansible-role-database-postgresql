# ansible-role-postgresql

Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:

      - name: database/etcd
          vars:
            # Defined by directory (look for individual server certificates)
            etcd_server_dir: /path/to/tls/certificates

            # or

            # Defined by file (look for a single server certificate)
            etcd_server: /path/to/tls/certificates
            etcd_ca: /path/to/tls/certificates
            etcd_interface: ens5

https://thenewstack.io/tutorial-set-up-a-secure-and-highly-available-etcd-cluster/

## Health Checks

etcdctl --endpoints https://192.168.10.1:2379 --cert /etc/etcd/server.crt --cacert /etc/etcd/etcd-ca.crt --key /etc/etcd/server.key put foo bar

etcdctl --endpoints https://192.168.10.1:2379 --cert /etc/etcd/server.crt --cacert /etc/etcd/etcd-ca.crt --key /etc/etcd/server.key get foo

curl --cacert /etc/etcd/etcd-ca.crt --cert /etc/etcd/server.crt --key /etc/etcd/server.key https://192.168.10.1:2379/health

etcdctl --endpoints https://192.168.10.1:2379 --cert /etc/etcd/server.crt --cacert /etc/etcd/etcd-ca.crt --key /etc/etcd/server.key member list


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
