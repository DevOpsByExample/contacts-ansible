# Contacts App
Ansible playbook to setup Contacts App

## Usage

```code
$ brew install ansible

# Clone this repo and edit the hosts.yml production/vagrant section

# To run against vagrant machine
$ ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook  --private-key=.vagrant/machines/default/virtualbox/private_key  -l vagrant -u vagrant  -i hosts.yml site.yml

# To provision the setup (one-time process)
$ ansible-playbook -l <vagrant|production> -u <ssh_user> -i hosts.yml site.yml

# Subsequently to deploy
$ ansible-playbook -l <vagrant|production> -u <ssh_user> -i hosts.yml -t deploy site.yml
```
