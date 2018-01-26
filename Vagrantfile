# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |vb|
  #   vb.gui = true
    vb.memory = "2048"
    vb.cpus = 2
  end
  
  config.vm.define "u1" do | u1 |
    u1.vm.box = "ubuntu/xenial64"
    u1.vm.network "private_network", ip: "10.0.0.11"
    u1.vm.hostname = "u1"
  end

  config.vm.define "u2" do | u2 |
    u2.vm.box = "ubuntu/xenial64"
    u2.vm.network "private_network", ip: "10.0.0.22"
    u2.vm.hostname = "u2"
  end

  config.vm.define "c1" do | c1 |
    c1.vm.box = "centos/7"
    c1.vm.network "private_network", ip: "10.0.0.33"
    c1.vm.hostname = "c2"
  end

  config.vm.provision "shell", inline: <<-SHELL
    date
    echo Done!
  SHELL
end
