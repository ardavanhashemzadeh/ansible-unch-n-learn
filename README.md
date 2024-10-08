# Ansible Lunch and Learn
```
1. Install AWX Operator into Rancher Desktop's K8s

2. ABCTJ: Ansible Basics, Common Terms and Jargon
    Basics
    a. What is Ansible ?
    b. What is Ansible Like?
    c. What is Like Ansible?

    Common Terms and Jargon:
    a. Control Node
    b. Managed Nodes
    c. Inventory
    d. Task
    e. Module
    f. Role
    g. Playbook
    h. Collection

```

```
https://ansible.readthedocs.io/projects/awx-operator/en/latest/installation/basic-install.html
https://docs.ansible.com/ansible-core/2.17/getting_started/index.html
https://github.com/ardavanhashemzadeh/ansible-unch-n-learn
```

```
echo '- src: idealista.superset_role
  scm: git
  version: 1.1.0
  name: superset_role
' > requirements.yml
ansible-galaxy install -p roles -r requirements.yml -f
echo '---
- hosts: all
  roles:
    - role: superset_role
' > install_superset.yml
ansible-playbook install_superset.yml -b -i INVENTORY
```