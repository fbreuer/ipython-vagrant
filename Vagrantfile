# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "puppetlabs/ubuntu-13.10-64-nocm"

  config.vm.network "forwarded_port", guest: 8888, host: 8889
  config.vm.network "forwarded_port", guest: 5006, host: 5007

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "_config/playbook.yml"
    #ansible.inventory_path = "provisioning/hosts-vagrant"
    # On Vagrant < 1.3 this used to be `inventory_file`...
    # ansible.inventory_file = "provisioning/hosts-vagrant"
    ansible.verbose = false
  end
end
