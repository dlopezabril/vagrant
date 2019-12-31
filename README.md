# vagrant
Vagrant Automation Projects

> **Create directory**
```shell
mkdir -p ~/Workspaces/vagrant/centos7
```
```shell
cd ~/Workspaces/vagrant/centos7
```

> **Generate and modify Vagrantfile**
```shell
vagrant init centos/7
```

> **Install vagrant-vbguest**
```shell
vagrant plugin install vagrant-vbguest
```

> **Edit Vagrantfile**
```shell
sublime Vagrantfile
```
> **Vagrantfile for centos/7 and ip "10.42.0.15"**
```shell
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "10.42.0.15"
end
```

> **Vagrant Commands**
```shell
vagrant up
```
```shell
vagrant reload
vagrant status
vagrant ssh
vagrant halt
vagrant destroy -f
```

> **ssh to vm from the shell**
```shell
ssh -i ~/Workspaces/vagrant/centos7/.vagrant/machines/default/virtualbox/private_key -p 22 vagrant@10.42.0.15
```

---

!!! note Refs

[Installing Your First Vagrant Box to Run VMs](https://blog.ipswitch.com/installing-your-first-vagrant-box)

[Vagrant Cheat Sheet · GitHub](https://gist.github.com/wpscholar/a49594e2e2b918f4d0c4)
!!!

---

!!! note Extras
```shell
[all:vars]
ansible_user=vagrant
ansible_ssh_pass=vagrant
ansible_ssh_host=10.42.0.15
ansible_ssh_port=22
ansible_ssh_user='vagrant'
ansible_ssh_private_key_file=~/Vagrant/CentOS7/.vagrant/machines/default/virtualbox/private_key
```
!!!