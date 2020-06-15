Vagrant.configure("2") do |config|

    config.vm.define "ubuntu1804" do |ubuntu1804|

        config.vm.box = "ubuntu/bionic64"
        config.vm.network :public_network, :bridge => "en0: Wi-Fi (Wireless)"
        config.vm.synced_folder "/Users/zaki/Documents/cilsy/sandbox/ubuntu1804", "/home/vagrant/host"
        config.vm.box_check_update = false

        config.vm.provision "shell", inline: <<-SHELL
            apt-get -y update
            apt-get install git nginx php php-mysql mysql-server
        SHELL
        
    end
end
