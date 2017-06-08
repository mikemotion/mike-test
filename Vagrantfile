Vagrant.configure("2") do |config|
  config.vm.box = "krrrunch/php-dev"

  config.vm.define "apps-mike-test" do |config|
    config.vm.hostname = "apps-mike-test"
    config.vm.network "private_network", ip: "192.168.33.39"
    # config.vm.network "forwarded_port", guest: 8080, host: 8080 # guest = VM, host = pc

    # config.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "my_id_rsa.pub"
    config.vm.provision "shell", path: "bootstrap.sh"

    config.vm.provider "virtualbox" do |v|
      v.cpus = 3
      v.memory = 3072
    end
  end
end
