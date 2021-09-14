
DOMAIN        = "vagrant.local"
NODE_COUNT    = 3
BASE_BOX      = "archlinux/archlinux"

Vagrant.configure("2") do |config|
    config.ssh.insert_key = false

    (1..NODE_COUNT).each do |i|
        config.vm.define "node#{i}" do |node|
            node.vm.box = BASE_BOX

            node.vm.hostname = "node#{i}.#{DOMAIN}"
            node.vm.network "private_network", ip: "172.30.0.#{i+100}"
        end
    end
end