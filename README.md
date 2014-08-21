To install ansible stuff:

vagrant install:

```bash
ansible-playbook -i vm_hosts provision.yml -u vagrant -k -c paramiko

# might work as well...
ansible-playbook -i vm_hosts provision.yml -k -c paramiko
ansible-playbook -i vm_hosts provision.yml
```

### digital ocean installation:

```bash
ansible-playbook -i hosts initial_bootstrap.yml

ansible-playbook -i hosts provision.yml -K

ansible-playbook -i hosts site.yml
```

### Generate password for user module

```bash
pip install passlib
python -c "from passlib.hash import sha512_crypt; print sha512_crypt.encrypt('<password>')"
```

Once the library is ready, SHA512 password values can then be generated

### postgresql backups
```
pg_dump --clean --no-owner --no-privileges
```
