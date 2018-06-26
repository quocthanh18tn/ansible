# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "bento/ubuntu-16.04"
  config.ssh.insert_key = false


  config.vm.provider :virtualbox do |v|
    v.memory = 256
    v.linked_clone = true
  end

  config.vm.define :app1 do |app|
    app.vm.hostname = "app1.test"
    app.vm.network :private_network, ip: "192.168.60.4"
  end

  config.vm.define :app2 do |app|
    app.vm.hostname = "app2.test"
    app.vm.network :private_network, ip:"192.168.60.5"
  end

  config.vm.define :db do |db|
    db.vm.hostname = "db.test"
    db.vm.network :private_network, ip:"192.168.60.6"
  end


end
