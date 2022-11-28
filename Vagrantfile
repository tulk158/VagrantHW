# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu_jammy64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provider "virtualbox" do |vb|
  vb.name = "bubunta666"
  vb.memory = "2000"
  vb.customize ["modifyvm", :id, "--vrde", "on"]
  vb.customize ["modifyvm", :id, "--vrdeport", "3389-3389"]
  end
 
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
	apt-get install -y googler
	apt-get install -y nnn
  SHELL
end
