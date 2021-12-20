# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "peru/ubuntu-20.04-server-amd64"
  config.vm.network "public_network"

config.vm.synced_folder ".", "/vagrant", type: "rsync", rsync_auto:
true, rsync_verbose: true
config.vm.provision "ansible_local" do |ansible|
ansible.verbose = true
ansible.playbook = "playbook1.yml"
 end
config.vm.provider "virtualbox" do |v|
v.memory = 2048
 end
end
