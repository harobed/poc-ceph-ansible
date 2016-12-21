# Prerequisites

Install Ansible and Vagrant:

```
$ brew install ansible
$ brew cask install virtualbox
$ brew cask install vagrant
$ brew install homebrew/completions/vagrant-completion
```

```
$ vagrant plugin install vagrant-hostmanager
$ vagrant plugin install vagrant-multiprovider-snap # To take snapshot, useful to debug
```

# Start VMs

```
$ vagrant up
```

# Test ping

```
$ ansible all -m ping -o -vv
```

# Install

```
$ ansible-playbook ../playbooks/install.yml
```

Check installation:

```
$ ansible-playbook ../playbooks/check.yml
```

# Configure client nodes

```
$ ansible-playbook ../playbooks/configure-clients.yml
```

# Create some Ceph block device image

```
$ ansible-playbook ../playbooks/create_block_devices.yml
```


# Clear cache

```
$ rm -rf hosts/.cache
$ rm -rf fetch/
```
