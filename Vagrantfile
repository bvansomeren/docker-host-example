# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vbguest.no_remote = true
  config.vbguest.auto_update = false
 
  config.vm.define 'centos7' do |instance|
    instance.vm.box = 'geerlingguy/centos7'
    config.vm.network :private_network, ip: "192.168.33.10"
    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "4096"]
        vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup.yml"
    ansible.groups = {
	"docker" => ["centos7"]
    }
  end
end
