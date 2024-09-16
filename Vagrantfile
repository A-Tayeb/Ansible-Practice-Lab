# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end
  
  config.vm.define "control" do |control|
    control.vm.box = "generic/oracle8"
    control.vm.hostname = "control"
    control.vm.network "private_network", ip: "192.168.56.10"
  end  
  config.vm.define "node1" do |node1|
    node1.vm.box = "generic/oracle8"
    node1.vm.hostname = "node1"
    node1.vm.network "private_network", ip: "192.168.56.11"
  end  
  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/debian-12"
    node2.vm.hostname = "node2"
    node2.vm.network "private_network", ip: "192.168.56.12"
  end
end