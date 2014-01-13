Description
===========

Collection of ansible playbooks to deploy virtual hybrid clusters in cloud infrastructures.

It includes playbooks to install openvpn 2.3.2 (creates a VPN network to interconnect all working nodes with the frontend) and Torque 4.2.5 + Maui 3.3.1 as a LRMS

Usage
=====

``` 
system section:
  disk.0.applications contains (name='ansible.modules.amcaar/ansible-playbook-hybrid-clusters') 

configure section:
  - include: clusters/tasks/openvpn-wn.yml
  - include: clusters/tasks/torque-wn.yml
  - include: clusters/tasks/openvpn-master.yml
  - include: clusters/tasks/torque-master.yml
```
