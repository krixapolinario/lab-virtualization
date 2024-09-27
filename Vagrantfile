# box = "centos/8"
# box_version = "1905.1"

# box = "debian/buster64"
# box_version = "10.20231211.1"

# box = "ubuntu/trusty64"
# box_version = "20191107.0.0"

Vagrant.require_version ">=2.3.6"
Vagrant.configure("2") do |config|
  config.vm.box = <INSERT_BOX>
  config.vm.box_version = <INSERT_BOX_VERSION>
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8192"
    vb.cpus = "2"
  end
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 9000, host: 9000
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/main.yml"
  end
end
