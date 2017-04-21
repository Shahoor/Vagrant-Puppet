Vagrant.configure("2") do |config|
  config.vm.provision :shell, path: "essentials.sh"
  config.vm.define "master" do |master|       
    master.vm.box = "puppetlabs/centos-7.2-64-puppet"
    master.vm.network "private_network", ip: "172.28.128.3"
      config.vm.provider "virtualbox" do |v|
        v.customize [ "modifyvm", :id, "--memory", "2048" ]
        v.customize [ "modifyvm", :id, "--cpus", "2" ]
      end
  end

  config.vm.define "agentone" do |agentone|
    agentone.vm.box = "puppetlabs/centos-7.2-64-puppet"
    agentone.vm.network "private_network", ip: "172.28.128.4"
  end
end
 