# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu/trusty64'
  config.vm.box_url = 'https://atlas.hashicorp.com/ubuntu/trusty64'
  config.vm.network 'forwarded_port', guest: 5900, host: 5901

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
  end

  config.vm.provider :virtualbox do |vb|
    vb.memory = 1024
    vb.cpus = 2
  end
end
