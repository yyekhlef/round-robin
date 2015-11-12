Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus = 2
    v.name = "ansible_tp7"
  end

  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.network "private_network", ip: "192.168.50.4"

  config.vm.define "haproxy" do |host|
    host.vm.hostname = "haproxy"
  end
end
