# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.ssh.insert_key = false
config.vm.provider :virtualbox do |vb|
vb.customize ["modifyvm", :id, "--memory", "1024"]
 end

 # control
 config.vm.define "chef-workstation" do |app|
 app.vm.hostname = "chef-workstation"
 app.vm.box = "bento/centos-7.2"
 app.vm.network :private_network, ip: "10.10.10.10"
 end
 
 
 # Load Balancer.
 config.vm.define "chef-server" do |app|
 app.vm.hostname = "chef-server"
 app.vm.box = "bento/centos-7.2"
 app.vm.network :private_network, ip: "10.10.10.11"
 end
 
 # Application server 1.
 config.vm.define "chef-client" do |app|
 app.vm.hostname = "chef-client"
 app.vm.box = "bento/centos-7.2"
 app.vm.network :private_network, ip: "10.10.10.12"
 end

 
 end
