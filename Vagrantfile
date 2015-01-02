Vagrant.configure("2") do |config|
    config.omnibus.chef_version = :latest
    config.berkshelf.enabled = true

    config.vm.box = "hashicorp/precise32"
    config.vm.box_url = "http://files.vagrantup.com/precise32.box"

    config.vm.host_name = "nh-api"

    config.vm.network "forwarded_port", guest:3000, host:3000

    config.vm.provision :shell, :path => "provision/provision.sh"

    config.vm.provision :chef_solo do |chef|
      chef.cookbooks_path = ["cookbooks"]
      chef.add_recipe "build-essential"
      chef.add_recipe "python"
      chef.add_recipe "nodejs"
      chef.add_recipe "mongodb"
    end
end