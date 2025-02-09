Vagrant.configure("2") do |config|
 
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "public_network"
  config.vm.synced_folder "C:/Users/eliez/Documents/Códigos Github/Projetos Vagrant/vagrant-ubuntu/root", "/home/vagrant/root" 
  config.vm.hostname = "vagrant-ubuntu"
  config.vm.provider "vmware_desktop" do |vmware|
    vmware.memory = 1024   # 1 GB de RAM
    vmware.cpus = 1        # 1 núcleo de CPU
  end
  
end
