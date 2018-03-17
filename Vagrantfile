# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos/7"

  config.vm.define "registry.docker" do |db|
    db.vm.network :private_network, ip: "10.0.0.10"
  end

  config.vm.define "node1.docker" do |www|
    www.vm.network :private_network, ip: "10.0.0.11"
  end

  config.vm.provision "shell", inline: <<-SHELL
     adduser ansible
     mkdir -p /home/ansible/.ssh
     cat /vagrant/vagrant_rsa.pub >> /home/ansible/.ssh/authorized_keys
     chown ansible /home/ansible/.ssh/authorized_keys
     chgrp ansible /home/ansible/.ssh/authorized_keys
  SHELL

end
