Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/bionic64"
  
    config.vm.define "wordpress" do |wordpress|
         wordpress.vm.network "private_network", type: "dhcp"
  
       config.vm.provision "shell",
       inline: "sudo apt-get update -y"   
    end
  
    config.vm.define "mysql" do |mysql|
       mysql.vm.network "private_network", type: "dhcp"
  
       config.vm.provision "shell",
       inline: "sudo apt-get update -y"  
    end
  
    config.vm.provider "virtualbox" do |v|
         v.memory = 1024
    end
  end
  