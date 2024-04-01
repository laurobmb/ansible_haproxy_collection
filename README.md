# Ansible Collection - laurobmb.statusinvest

Documentation for the collection.

### Galaxy collection build
> ansible-galaxy collection build
### Galaxy collection install from file
> ansible-galaxy collection install laurobmb-statusinvest-1.0.0.tar.gz
### Galaxy collection install from git
> ansible-galaxy collection install git+https://github.com/laurobmb/ansible_statusinvest_collection.git,main

> ansible-galaxy collection install laurobmb-statusinvest-1.0.4.tar.gz -p collections/

### Playbook sample
    ---
    - name: Install HAproxy with KeepAlived
      hosts: haproxy_groups
      vars:
        
      keepalived_virtualip: 10.36.39.200
      
      web_servers:
        - 192.168.11.10
        - 192.168.11.11
        - 192.168.11.12
        - 192.168.11.13

      tasks:
        - name: Import role
          ansible.builtin.import_role:
            name: laurobmb.haproxy.install_haproxy
        
        - name: Import role
          ansible.builtin.import_role:
            name: laurobmb.haproxy.install_keepalived
    