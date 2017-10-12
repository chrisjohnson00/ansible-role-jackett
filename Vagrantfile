# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

#jacket
  config.vm.network "forwarded_port", guest: 9117, host: 9117


  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1

          ## fixes https://github.com/chef/bento/issues/688
            vb.customize ["modifyvm", :id, "--cableconnected1", "on"]
            vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end


config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.sudo = true
    ansible.verbose = true #set this to true if you want to see all the output
    ansible.limit = "all"
  end

end
