To install ansible stuff:

vagrant install:
ansible-playbook -i vm_hosts provision.yml -u vagrant -k -c paramiko
# might work as well...
ansible-playbook -i vm_hosts provision.yml -k -c paramiko
ansible-playbook -i vm_hosts provision.yml

digital ocean installation:
ansible-playbook -i hosts initial_bootstrap.yml
/*Make sure the sudo password is entered*/
ansible-playbook -i hosts provision.yml -K

--- 14-06-2014
ansible-playbook -i hosts site.yml


Generate password for user module
pip install passlib
Once the library is ready, SHA512 password values can then be generated as follows:

python -c "from passlib.hash import sha512_crypt; print sha512_crypt.encrypt('<password>')"

postgresql backups:
pg_dump --clean --no-owner --no-privileges
