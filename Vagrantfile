# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  
   config.vm.box = "debian/jessie64"
  
   config.vm.box_check_update = false

   # Disable the default /vagrant share
   config.vm.synced_folder "../data", "/vagrant_data" , disabled: true

<<<<<<< HEAD
   config.vm.define "ansible-vm" do |cfg|
    cfg.vm.network "private_network", ip: "192.168.33.10"
    cfg.vm.hostname = "ansible-vm"    
=======
   config.vm.define "ansible_vm" do |cfg|
    cfg.vm.network "private_network", ip: "192.168.33.101"
    cfg.vm.hostname = "ansible_vm"    
>>>>>>> fa3edf0d9280015a1d2c10e298764b791b70cf75
    cfg.vm.provider "virtualbox" do |vb|
     vb.gui = true
     vb.name = 'ansible-vm'
     vb.memory = "1200"
    end
    cfg.vm.provision :ansible do |ansible|
     ansible.playbook = 'provision.yml'
     ansible.inventory_path = 'vagrant-inventory.ini'
     ansible.limit = 'ansible-vm'
     ansible.verbose = 'v'
    end
   end
end
