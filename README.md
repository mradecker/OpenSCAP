# OpenSCAP
# Ansible playbook to install OpenSCAP and scan hosts for security compliance 

# Ensure that you have Ansible installed on your system before running the playbook.  You will need to run 
# these commands to install the following packages.

yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum install ansible

# After installing Ansible, you will have to specify your inventory in /etc/ansible/hosts.
# Check out https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html for help with inventory file

# After the inventory file has been updated, copy the openscap.yml to the directory of your choice.  
# For example, /opt/ansible/playbooks

# Here are a few options to fun the playbook
ansible-playbook openscap.yml
ansible-playbook openscap.yml -vv  (use this to make it verbose)
ansible-playbook -u <user_name> openscap.yml  (use this if you want to specify a certain user)
