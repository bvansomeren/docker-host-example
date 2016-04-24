# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vbguest.no_remote = true
  config.vbguest.auto_update = false
 
  config.vm.define 'centos7' do |instance|
    instance.vm.box = 'geerlingguy/centos7'
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup.yml"
    #ansible.verbose = 'v'
    ansible.groups = {
	"docker" => ["centos7"]
    }
  end
end
