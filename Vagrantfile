Vagrant.configure("2") do |config|
  config.vm.box = "aucix/elementary_aucix"
  config.vm.box_version = "1.2"
  
  config.vm.provider "virtualbox" do |virtualbox|
  virtualbox.gui = true
  virtualbox.cpus = 4
  virtualbox.memory = 8192
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.install_mode = "pip"
    ansible.version = "2.3.2.0"
    ansible.playbook = "playbook.yml"
  end

  config.vm.provision :reload
end
