# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'bento/ubuntu-16.04'
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :private_network, ip: '192.168.33.10'
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = 512
  end
  config.vm.provision :ansible do |ans|
    # where the playbook is location
    ans.playbook = 'provisioning/playbooks.yml'
  end
end
