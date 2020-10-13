# -*- mode: ruby -*-

Vagrant.configure("2") do |config|


  config.vm.define "web" do |web|
  web.vm.box = "debian/stretch64"
  web.vm.network "private_network", ip: "192.168.33.10"
  web.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    vb.cpus = 1
    end
  web.vm.provision  "playbook1", type:'ansible' do |ansible|
    ansible.playbook = 'ansible/wp.yml'
    end
  end

  config.vm.define "db" do |db|
  db.vm.box = "debian/stretch64"
  db.vm.network "private_network", ip: "192.168.33.20"
  db.vm.provider "virtualbox" do |vb|
    vb.memory = "486"
    vb.cpus = 1
    end
  db.vm.provision  "playbook2", type:'ansible' do |ansible|
    ansible.playbook = 'ansible/db.yml'
    end
  end

end
