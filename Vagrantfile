# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  ## Setup Ansible Server
  config.vm.define "acs" do |acs|
    acs.vm.box = "centos/7"
    acs.vm.hostname = "acs"    
    acs.ssh.forward_agent = true
    acs.vm.synced_folder "./devops_ci", "/mnt/shared"
    acs.vm.network "private_network", ip: "192.168.33.10"
  end

  # ## Setup Kafka
  # config.vm.define "kf" do |kf|
  #   kf.vm.box = "centos/7"
  #   kf.vm.hostname = "kf"
  #   kf.ssh.forward_agent = true
  #   kf.vm.network "private_network", ip: "192.168.33.20"    
  # end

  # ## Setup zookeeper
  # config.vm.define "zk" do |zk|
  #   zk.vm.box = "centos/7"
  #   zk.vm.hostname = "zk"
  #   zk.vm.network "private_network", ip: "192.168.33.30"
  # end


  # ## Setup zookeeper
  # config.vm.define "zk1" do |zk1|
  #   zk1.vm.box = "centos/7"
  #   zk1.vm.hostname = "zk1"
  #   zk1.vm.network "private_network", ip: "192.168.33.40"
  # end

end