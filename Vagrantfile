# -*- mode: ruby -*-
# vi: set ft=ruby :

#for Vagrant >1.2.x
Vagrant.configure("2") do |config|
    config.vm.provision :shell, :inline => "echo Welcome to CockRoachApp VM"

    config.vm.define :dev do |_config|
        _config.vm.box = "trisoft/cockroachapp-201705140946"

        _config.vm.hostname = "cr"

        _config.vm.synced_folder ".", "/var/www", :nfs => true

        _config.vm.provision "file", source: "~/.ssh/id_rsa", destination: "~/.ssh/id_rsa"

        _config.vm.provider :virtualbox do |vb, override|
            vb.customize ["modifyvm", :id, "--memory", 4096]
            vb.customize ["modifyvm", :id, "--cpus", "4"]
            override.vm.box_url = "http://labs.io.trisoft.ro/box/cockroachapp-201705140946.box"
            override.vm.network :private_network, ip: "192.168.33.178"
        end
    end
end
