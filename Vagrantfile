# -*- mode: ruby -*-
# vi: set ft=ruby :

  Vagrant.configure("2") do |config|
#  config.proxy.http     = "http://5.252.21.97:8080"
#  config.proxy.https    = "https://5.252.21.97:8080"
#  config.proxy.no_proxy = "localhost,127.0.0.1"

  config.vm.network "forwarded_port", guest: 3000, host: 3000

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.box = "generic/ubuntu2004"
  config.vm.provider "virtualbox" do |vb|
     vb.name = "astratest"
     vb.gui = false
     vb.memory = "2048"
     vb.cpus = 2
  end
end
