# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version.
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.ssh.insert_key = false
    config.ssh.private_key_path = "~/.vagrant.d/insecure_private_key"

    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
        v.cpus = 1
    end

    config.vm.define "docker-host" do |box|
        box.vm.hostname = "docker-host"
        box.vm.box = "ubuntu/trusty64"

        box.vm.network :private_network, ip: "192.168.60.2"
        config.ssh.forward_agent = true # allow external SSH
    end
end

