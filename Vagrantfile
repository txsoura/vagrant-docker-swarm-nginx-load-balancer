Vagrant.configure("2") do |config|
config.vm.box = "ubuntu/focal64"

    config.vm.define :balancer do |balancer|
      balancer.vm.provider "virtualbox" do |vb|
        vb.cpus = 1
        vb.memory = "512"
      end

      balancer.vm.network :private_network, ip: "172.72.72.10"
      balancer.vm.hostname = "balancer"
      balancer.vm.provision :shell, inline: "sudo apt-get update && sudo curl -fsSL https://get.docker.com | sh"
    end
  
    config.vm.define :one do |one|
      one.vm.provider "virtualbox" do |vb|
        vb.cpus = 1
        vb.memory = "512"
      end

      one.vm.network :private_network, ip: "172.72.72.20"
      one.vm.hostname = "one"
      one.vm.provision :shell, inline: "sudo apt-get update && sudo curl -fsSL https://get.docker.com | sh"
    end
    
    config.vm.define :two do |two|
      two.vm.provider "virtualbox" do |vb|
        vb.cpus = 1
        vb.memory = "512"
      end

      two.vm.network :private_network, ip: "172.72.72.30"
      two.vm.hostname = "two"
      two.vm.provision :shell, inline: "sudo apt-get update && sudo curl -fsSL https://get.docker.com | sh"
    end
end
