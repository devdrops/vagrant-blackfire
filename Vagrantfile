
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  
  config.vm.network :private_network, ip: "192.168.0.1"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 8081, host: 8081

  config.vm.synced_folder "./dev", "/var/www/dev"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
  end

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.vm.hostname = 'silex-application.localhost'
end
