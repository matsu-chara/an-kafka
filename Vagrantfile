# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/centos-7.2"
  config.vm.network "private_network", ip: "192.168.33.15"

  config.vm.provision :ansible do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "site.yml"
  end

  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.scope = :box
  end

  if Vagrant.has_plugin?("vagrant-vbguest")
    # config.vbguest.auto_update = false
  end
end
