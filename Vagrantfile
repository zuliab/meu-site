Vagrant.configure("2") do |config|

  config.vm.box = "cloud-image/debian-13"
  config.vm.box_version = "20260501.2465.0"
  config.vm.box_check_update = false

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 22, host: 2222, id: "ssh"

  #config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  
  config.vm.network "private_network", ip: "192.168.0.2"
  #config.vm.network "public_network"

  config.vm.synced_folder "./meu-site", "/var/www/meu-site"

  # config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |vb|
  vb.name = "Vm-Ativ-Vagrant"

  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   
  # Customize the amount of memory on the VM:
  vb.memory = "1024"
  end
  #
    config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2

   chmod -R 755 /var/www/meu-site
   rm -rf /var/www/html
   ln -s /var/www/meu-site /var/www/html
   SHELL
   end
