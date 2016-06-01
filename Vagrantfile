# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos7"
  config.vm.box_url = "https://github.com/holms/vagrant-centos7-box/releases/download/7.1.1503.001/CentOS-7.1.1503-x86_64-netboot.box"

  config.vm.box_check_update = false

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.33.50"
  # config.vm.network "public_network"

  config.vm.synced_folder "./www/html", "/home/vagrant/dist/www/html", mount_options:['dmode=777','fmode=755']

  config.vm.provider "virtualbox" do |vb|
  #   vb.gui = true
    vb.memory = "1024"
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  end

  # config.vm.provision "ansible" do |ansible|
  #  ansible.limit = 'all'
  #  ansible.inventory_path = "ansible/hosts"
  #  ansible.playbook = "ansible/development.yml"
  # end

  # config.vm.provision :shell, run: "always", :inline => <<-EOT
  #  sudo service httpd restart
  #  sudo service mysqld restart
  # EOT
end
