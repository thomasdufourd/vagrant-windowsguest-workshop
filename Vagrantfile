# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# My provisioning script
#$script =  <<SCRIPT
#SCRIPT


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.guest = :windows 
  config.vm.box = "win2012-R2"
  # the 'base' box location URL : file or network resource, remote or local
  #config.vm.box_url = "file://{path_to_where_you_saved_the_box_file_local}/win2012-R2.box"

  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.network :forwarded_port, guest: 3389, host: 33389, id: "rdp", auto_correct: true
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.communicator = "winrm"

  # config.vm.synced_folder "../data", "/vagrant_data"

  # config.vm.provider "virtualbox" do |vb|
  #   # Use VBoxManage to customize the VM. For example to change memory:
  #   vb.customize ["modifyvm", :id, "--memory", "1024"]
  # end
  #


  # Provisioning
  #--------------
  # simple provisioning with a script (the script is inlined in a variable at the top of the Vagrantfile)
  #config.vm.provision "shell", inline: $script

  # Enable provisioning with Puppet stand alone.  Puppet manifests
  # are contained in a directory path relative to this Vagrantfile.
  # You will need to create the manifests directory and a manifest in
  # the file default.pp in the manifests_path directory.
  #
  # config.vm.provision "puppet" do |puppet|
  #   puppet.manifests_path = "manifests"
  #   puppet.manifest_file  = "default.pp"
  # end

end
