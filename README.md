# Launch or regenerate EC2 isntances with Ansible

## Ansible
* Read how to use the **Ansible** provisioner in README.md of each role.
* To know more about Ansible: http://www.ansible.com

### Dependencies

None

## Configuration:

UModify in your custon role the following variables:

https://github.com/Aplyca/ansible-role-ec2launch/blob/master/defaults/main.yml

## Launch instances

```bash
ansible-playbook -i inventories/local playbooks.yml
```

### Custom settings
In order to use your own custom settings, use the "tests/custom.yml" file, you can override any variable used in the playbooks and roles.

```bash
ansible-playbook -i inventories/local tests/playbooks.yml --extra-vars "@tests/custom.yml"
```

By default the tests-custom.yml file is ignored in git, be mindful to not add to version control your custom files or info.

## Tests
```bash
ansible-playbook -i inventories/local tests/playbooks.yml
```

## Version control
* Use git to push/push all your changes.
