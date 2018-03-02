# Contacts App
Ansible playbook to setup Contacts App


## Provision/deploy to vagrant box
Make sure you have Ansible, Virtualbox and Vagrant installed in your machine.

```code
# Clone this repo and CD into it.

$ vagrant up

$ ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook  --private-key=.vagrant/machines/default/virtualbox/private_key  -l vagrant -u vagrant  -i hosts.yml site.yml
```
App can be accessed at: http://192.168.5.100/ui

## Provision/deploy to a environment
Edit hosts.yml as required

```
# To provision the setup (one-time process)
$ ansible-playbook -l <staging|production> -u <ssh_user> -i hosts.yml site.yml

# Subsequently to deploy
$ ansible-playbook -l <staging|production> -u <ssh_user> -i hosts.yml -t deploy site.yml
```
