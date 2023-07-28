# -*- mode: ruby -*-

# vi: set ft=ruby :

 

# All Vagrant configuration is done below. The "2" in Vagrant.configure

# configures the configuration version (we support older styles for

# backwards compatibility). Please don't change it unless you know what

# you're doing.

Vagrant.configure("2") do |config|

  # The most common configuration options are documented and commented below.

  # For a complete reference, please see the online documentation at

  # https://docs.vagrantup.com.

 

  # Every Vagrant development environment requires a box. You can search for

  # boxes at https://vagrantcloud.com/search.

  config.vm.define "ansiblecontrol" do |ansiblecontrol|

    ansiblecontrol.vm.box = "generic/centos7"
    ansiblecontrol.vm.box_download_insecure = true
    ansiblecontrol.ssh.insert_key = false
    ansiblecontrol.vm.boot_timeout = 6000
    ansiblecontrol.vm.network "forwarded_port", guest: 80, host: 7282
    ansiblecontrol.vm.network "private_network", ip: "192.168.56.100"
    ansiblecontrol.vm.network "public_network"
    ansiblecontrol.vm.synced_folder "./vagrant_files", "/vagrant_data"
    ansiblecontrol.vm.provider "virtualbox" do |vb|       

      # Customize the amount of memory on the VM:
      vb.memory = "4096"
    end
  end
  config.vm.define "managenode1" do |managenode1|

    managenode1.vm.box = "generic/ubuntu2204"
    managenode1.ssh.insert_key = false
    managenode1.vm.boot_timeout = 6000
    managenode1.vm.box_download_insecure = true
    managenode1.vm.network "forwarded_port", guest: 80, host: 7283
    managenode1.vm.network "private_network", ip: "192.168.56.101"
    managenode1.vm.network "public_network"
    managenode1.vm.synced_folder "./vagrant_files", "/vagrant_data"
    managenode1.vm.provider "virtualbox" do |vb|       

      # Customize the amount of memory on the VM:
      vb.memory = "1024"
    end
  end
  config.vm.define "managenode2" do |managenode2|

    managenode2.vm.box = "generic/ubuntu2204"
    managenode2.ssh.insert_key = false
    managenode2.vm.boot_timeout = 6000
    managenode2.vm.box_download_insecure = true
    managenode2.vm.network "forwarded_port", guest: 80, host: 7284
    managenode2.vm.network "private_network", ip: "192.168.56.102"
    managenode2.vm.network "public_network"
    managenode2.vm.synced_folder "./vagrant_files", "/vagrant_data"
    managenode2.vm.provider "virtualbox" do |vb|       

      # Customize the amount of memory on the VM:
      vb.memory = "1024"
    end
  end
end

 