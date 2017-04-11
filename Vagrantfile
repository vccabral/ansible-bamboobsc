Vagrant.configure("2") do |config|
  config.vm.box = "base"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "bamboobsc_installation.yml"
    ansible.verbose = "v"
    ansible.groups = {
        "bamboobscnode" => ["default"],
    }
  end
end
