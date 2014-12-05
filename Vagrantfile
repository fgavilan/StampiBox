# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

#config.vm.define :compos do |compos|
#  compos.vm.box = "Compos"
#  compos.vm.network "forwarded_port", guest: 80, host: 8080
#  compos.vm.network "forwarded_port", guest: 5432, host: 5432
#  compos.vm.synced_folder "/home/COMPOS/rodolfo/projetos", "/vagrant"
#end

config.vm.define :ubuntu do |ubuntu|
  ubuntu.vm.box = "ubuntu"
  ubuntu.vm.network "forwarded_port", guest: 80, host: 8081
  ubuntu.vm.network "forwarded_port", guest: 5433, host: 5435
  ubuntu.vm.synced_folder "/home/byhours/vagrant_dev/ubuntu", "/vagrant"
  ubuntu.vm.synced_folder "/home/byhours/Documentos/git/", "/var/www/"
end


#config.vm.box = "Compos"
#  config.vm.network "forwarded_port", guest: 80, host: 8080
#  config.vm.network "forwarded_port", guest: 5432, host: 5432

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  # config.vm.box_url = "http://domain.com/path/to/above.box"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network :forwarded_port, guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network :private_network, ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network :public_network

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"
  #  config.vm.synced_folder "/home/COMPOS/albertoromero/projetos", "/vagrant"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
   config.vm.provider :virtualbox do |vb|
  #   # Don't boot with headless mode
  #   vb.gui = true
  #
  #   # Use VBoxManage to customize the VM. For example to change memory:
     vb.customize ["modifyvm", :id, "--memory", "512"]
   end

end
