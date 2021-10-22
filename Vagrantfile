# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "generic/fedora34"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus   = 2
  end

  config.vm.provider "libvirt" do |v|
    v.memory = 2048
    v.cpus   = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo dnf install -y livecd-tools
  SHELL
end
