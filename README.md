# global-ansible-repo
Will host ansible roles for things I find myself needing

## TODO
* include my meta handelers file, and meta handlers role
* export variables in a meta way. Example: existence of public or internal firewalld zone files

## Running
To run a single role, you would do something like the following:
```bash
ansible HOSTLIST -i hosts --module-name include_role -C -D --args name=ROLE_NAME
```
To run a single playbook, you would do something like the following:
```bash
ansible-playbook -i hosts -C -D playbooks/PLAYBOOK/main.yml
```
Finally, to run the entire prod_site.yml, you would do the following
```bash
ansible-playbook -l HOSTLIST -i hosts -C -D prod_site.yml
```
