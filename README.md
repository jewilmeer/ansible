To install ansible stuff:

vagrant install:
ansible-playbook -i vm_hosts provision.yml -u vagrant -k -c paramiko
