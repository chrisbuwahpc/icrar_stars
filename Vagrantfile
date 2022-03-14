# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
   Vagrant.configure("2") do |config|

   config.vm.box = "UWA-HPC/icrar22"
   config.vm.box_version = "1.0.0"

   config.ssh.forward_agent = true
   config.ssh.forward_x11 = true
   config.vm.network "forwarded_port", guest: 2222, host: 2222
  # argument is a set of non-required options.
   config.vm.synced_folder "images_shared", "/home/vagrant/images_shared"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
   config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
     vb.cpus = "2"
  #   # Customize the amount of memory on the VM:
     vb.memory = "4096"
   end

   config.vm.host_name = "starlight"

   config.vm.provision "shell", privileged: false, path: "Vagrant_provision.sh"
   
end
