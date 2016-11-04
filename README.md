# rsfo for Ansible version
==========================

Rapid Setting For Oracle (RAC)
------------------------------

### What is RSFO for Ansible?

RSFO is a package, distributed as an Ansible role, that automates all the pre-requisite tasks for an Oracle installation on Red Hat 7.

### How to prepare your environment for using RSFO

1. Create a devops:users in the main target installation node.
2. sudo root for devops without password.
3. (optional) configure the cluster interconnect or the network in case of multiple single instance installation.
4. configure the ssh for root without password nor passphrase between the master target node and the cluster nodes (in case of multinode like RAC installation).

### How to use RSFO for Ansible in a single node deployment context

1. Download the latest Ansible role (rsfo_ansible.tar.gz) from the Github page https://github.com/yannallandit/rsfoansible
2. Install the role: tar xzvf rsfo_ansible.tar.gz
3. Update the variable file located in ./yannallandit.rsfo/vars/main.yml
4. Implement the role in your playbook as in the example provided: testrsfo.yml
5. More details are provided in the file ./yannallandit.rsfo/README.md

More information, look at the RSFO_Ansible_Introduction_V1a.pdf and at https://github.com/yannallandit/rsfo

