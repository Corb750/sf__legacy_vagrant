# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant development environment requires a box. You can search for
  # hashicorp/bionic64 - Ubuntu 18.04.6 LTS Bionic Beaver September 17.2021
  # ubuntu/focal64 - Ubuntu 20.04.4 LTS Focal Fossa February 24, 2022
  # bento/ubuntu-20.04  - Ubuntu 20.04.4 LTS Focal Fossa February 24, 2022
  # https://wiki.ubuntu.com/Releases
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/focal64"  

  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu-pg84"
    vb.memory = "2048"
    vb.cpus = 2
  end

  config.vm.hostname = "newapp"

  config.vm.hostname = "ubuntu-pg84"
  config.vm.network "forwarded_port", guest: 5432, host: 5432 
  config.vm.network "private_network", ip: "192.168.10.100"

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available.
  # SHELL
  config.vm.provision "shell", path: "provision.sh"
end
