# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-24.04" # Ubuntu 22.04 LTS
  config.vm.box_version = "202404.26.0"

  config.vm.network "public_network", ip: "192.168.0.99"
#  config.vm.network "public_network"
  config.vm.provision "shell", inline: <<-SHELL
#  config.vm.provider "virtualbox" do |vb|
    vb.nome = "node1"
    sudo apt-get update
    sudo apt-get install -y docker.io
    sudo systemctl start docker
    sudo systemctl enable docker
    sudo usermod -aG docker vagrant
  SHELL
end


