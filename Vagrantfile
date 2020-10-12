# -*- mode: ruby -*-

Vagrant.configure("2") do |config|

  config.vm.define "web_sever"
  config.vm.box = "debian/stretch64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provider "virtualbox" do |vb|
   vb.memory = "256"
   vb.cpus = 1
   end

  config.vm.define "db"
  config.vm.box = "debian/stretch64"
  config.vm.network "private_network", ip: "192.168.33.20"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "256"
    vb.cpus = 1
  end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
  config.vm.provision "ansible" do |ansible|
     ansible.playbook = "ansible/apache2.yml"
     ansible.playbook = "ansible/db.yml"
   end
end
