Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - name: Generate Kubernetes Worker Golden Image
      hosts: all
      become: yes
      become_user: root
      gather_facts: yes
      roles:
        - role: centos
        - role: k8sworker
          k8s_ca_cert: "ca.pem"
          k8s_ca_key: "ca-key.pem"
          k8s_version: "v1.20.2"
          crio_enable: false
          containerd_enable: true
          cert_country: "BR"
          cert_city: "Sao Paulo"
          cert_state: "SP"
          cntlr_cidr: "10.1.0.0/24"
          loadbalancer_ip: "10.1.0.40"

License
-------

BSD

Author Information
------------------

[Luis Gomes](https://github.com/luishmg/luishmg.github.io)
