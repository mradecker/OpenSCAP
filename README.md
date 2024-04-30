### This playbook will install OpenSCAP and scan hosts for security compliance.  OpenSCAP will scan hosts and create a remediation playbook, XML results file, and HTML report.  

### If the playbook is being run on a cluster, the results and report files will be fetched from the nodes to the basebox for easy access.

### Ensure that you have Ansible installed on your system before running the playbook.  You will need to run these commands to install the following packages.  

### yum install ansible

### Further installation instructions can be found at https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

### After installing Ansible, you will have to specify your inventory in /etc/ansible/hosts.
### Check out https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html for help with inventory file

### After the inventory file has been updated, copy the openscap.yml to the directory of your choice and run it from that directory so you don't have to include the path to the directory in your command.
### For example, /opt/ansible/playbooks

### Here are a few options to fun the playbook

### sudo ansible-playbook openscap.yml
### sudo ansible-playbook openscap.yml -vv  (use this to make it verbose)
### sudo ansible-playbook -u <user_name> openscap.yml  (use this if you want to specify a certain user)
### sudo ansible-playbook -vvbkKu <user_name> openscap.yml (specify user, prompt for ssh password, prompt for sudo password, verbose)

### If running the playbook as root, you can run the following commands
### ansible-playbook openscap.yml -vv
### ansible-playbook openscap.yml -vvk (-k prompts for ssh password which is needed to communicate with cluster nodes)
