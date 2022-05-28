Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.ssh.insert_key = false
  config.vm.provision :docker
  config.vm.provision :docker_compose, run: "always"
  config.vm.network "forwarded_port", guest: 80, host: 8081
#  config.vm.network "forwarded_port", guest: 389, host: 389
#  config.vm.network "forwarded_port", guest: 636, host: 636
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 9090, host: 9090
  config.vm.network "forwarded_port", guest: 9100, host: 9100
  config.vm.network "forwarded_port", guest: 9100, host: 9100
  config.vm.network "forwarded_port", guest: 9093, host: 9093
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.provider "virtualbox" do |vb|
    #  vb.gui = true
       vb.name = "ubuntu-docker"
       vb.memory = "2048"
     end
end