Vagrant.configure("2") do |config|

    config.vm.provider :virtualbox do |v|
        v.name = "ansible.davidcorto.es"
        v.customize ["modifyvm", :id, "--memory", 1024]
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end

    config.vm.box = "ubuntu/trusty64"

    config.vm.network :private_network, ip: "192.168.100.99"
    config.ssh.forward_agent = true

    # Folder share
    #config.vm.synced_folder "./", "/vagrant", type: "nfs"
    config.vm.synced_folder "./", "/vagrant", type: "virtualbox"

    # Run Ansible from the Vagrant Host
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "ansible/playbook.yml"
        ansible.verbose = true
    end

    # Run Ansible from the Vagrant VM
    #config.vm.provision "ansible_local" do |ansible|
    #    ansible.playbook = "ansible/playbook.yml"
    #    #ansible.verbose = true
    #    ansible.vault_password_file = ".vault.txt"
    #    ansible.version = "2.2.0"
    #    ansible.install_mode = "pip"
    #end
end
