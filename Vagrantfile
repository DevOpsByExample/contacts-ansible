# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "192.168.5.100"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
  end
end
