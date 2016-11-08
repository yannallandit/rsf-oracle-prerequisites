<<<<<<< HEAD
Rapid Setting For Oracle Prerequisites
======================================

RSFO for Ansible is the Ansible role implementation of the Rapid Setting For oracle rpm.  
RSFO goal is to provide a set of scripts to enable a REDHAT 7 environment for Oracle 12c Single Instance or RAC.  
RSFO will set the Oracle pre-requesites except:
- The storage configuration
- The root ssh without password needed for deployement
- The network setting

Restriction:
------------

- Maximum nodes in the cluster: 12.
- These scripts has been designed for RedHat 7.
- Only the RH7 Update 1 is tested with the current build. However, nothing should prevent to use it with any RH7.x release.
- The ssh as to be set before you run the scripts.
- A YUM repository need to be reachable for the installation of the packages required by Oracle



Requirements
------------

A devops:users need to exist on the main target node. This one need to be able to sudo without password.  
The root user main target node needs also to be able to ssh the other cluster nodes without password of passphrase.

Role Variables
--------------

Before running this role you need to update the variables in vars/main.yml.  
The variables are:
- MAIN_NODE is the node from where Ansible will drive the deployment of RSFO.
- TARGET_NODES need to be defined in a case of multi-node deployment (preparation for RAC implementation for instance).
- GRID_BASE is the loation of the BASE directory for the GRID components.
- ORA_BASE is the loation of the BASE directory for the Oracle database components.

Dependencies
------------

This role only works with RHEL 7 as target operating system.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:  

   `---`  
   `- name: test module for RSFO`  
     `  hosts: "{{ MAIN_NODE }}"`  
     `  roles:`  
     `    - role: yannallandit.rsfo`  

License
-------

Apache V2

Author Information
------------------

yann.allandit@hpe.com
=======
# rsf-oracle-prerequisites
>>>>>>> 6d1aaa30efc965b9bb25655d533e10a21ad16a7f
