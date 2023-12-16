# Wordpress role for ansible

Installing and configuring wordpress and the necessary apache settings.
You will get a bare wordpress where you can log

## ToDo
* Customize vars/main.yaml according to your needs
  (You should encrypt passwords with ansible-vault:
   https://docs.ansible.com/ansible/latest/vault_guide/vault_encrypting_content.html)
* Copy the cloned repository in your ansible setup
  (If you don't have on you can take this:
   https://github.com/kdx99/ansible-structure)
* Edit the hosts file:
```
  [wordpress]
  server1.example.com
  server2.example.com
  ...
```
* Create playbook wordpress.yaml:
```
  - hosts: wordpress
  roles:
    - wordpress
```
* Run playbook:
```
  ansible-playbook wordpress.yaml
```

## Spoilers
* Does not run as multidomain wordpress
* Tested on debian (bookworm), nothing else
* apache proof, not nginx
* If you have already a configured an apache server, this role might change the settings
  -> you might want to make a backup first
