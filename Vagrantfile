# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.vm.network "forwarded_port", guest: 5002, host: 5002
  config.vm.network "forwarded_port", guest: 44319, host: 44319
  config.vm.network "public_network", bridged: ""
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end
  config.vm.provision "shell", inline: <<-SHELL
    # Install Docker
    wget -qO- https://get.docker.com/ | sh

    # Install Docker Compose
    curl -L https://github.com/docker/compose/releases/download/1.1.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose

    # Copy docker-compose file to root
    cp /vagrant/docker-compose.yml /root

    # Start API and database
    cd /root
    docker-compose up -d

    # Be happy.
    echo "___.   .__                   __            _____  _____._."
    echo "\\_ |__ |  | _____    _______/  |_    _____/ ____\\/ ____\\ |"
    echo " | __ \\|  | \\__  \\  /  ___/\\   __\\  /  _ \\   __\\\\   __\\ | |"
    echo " | \\_\\ \\  |__/ __ \\_\\___ \\  |  |   (  <_> )  |   |  |   \\|"
    echo " |___  /____(____  /____  > |__|    \\____/|__|   |__|   __"
    echo "     \\/          \\/     \\/                              \\/"
  SHELL
end
