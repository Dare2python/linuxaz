# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |vb|
  #   vb.gui = true
    vb.memory = "2048"
    vb.cpus = 2
  end
  
  config.vm.define "t1" do | t1 |
    t1.vm.box = "ubuntu/xenial64"
#   t1.vm.network "private_network", ip: "192.168.33.10"
    t1.vm.hostname = "t1"
  end

  config.vm.provision "shell", inline: <<-SHELL
    date
    echo Done!
  SHELL
end
