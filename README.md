This is a collection of scripts used to install servers I run for personal projects. Feel free to use them and make suggests / pull-requests. Since all this is for personal projects, it's only recommended to use as inspiration.

To install ansible stuff:
note: I've recently added `ansible-vault` files. Run vaulted scripts with `--vault-password-file ~/.vault_pass.txt` and place your pass in the given file. Example files will be provided

### vagrant install:

```bash
ansible-playbook -i vm_hosts provision.yml --vault-password-file ~/.vault_pass
```

### digital ocean installation:

```bash
ansible-playbook -i hosts initial_bootstrap.yml --vault-password-file ~/.vault_pass
ansible-playbook -i hosts provision.yml --vault-password-file ~/.vault_pass
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
