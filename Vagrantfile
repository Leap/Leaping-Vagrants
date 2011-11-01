Vagrant::Config.run do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu-1104-server-i386"

  config.vm.box_url = "http://dl.dropbox.com/u/7490647/talifun-ubuntu-11.04-server-i386.box"

  config.vm.forward_port("web", 8000, 8000)
  config.vm.network("33.33.00.10")
  
  config.vm.share_folder "leap-lite", "/home/vagrant/src/leap-lite", "../leap-lite"
  

  # Enable provisioning with chef solo, specifying a cookbooks path (relative
  # to this Vagrantfile), and adding some recipes and/or roles.
  #
  config.vm.provision :chef_solo do |chef|    
     chef.recipe_url = "http://files.vagrantup.com/getting_started/cookbooks.tar.gz"
     chef.cookbooks_path = "cookbooks"
     chef.add_recipe "main"
     chef.add_recipe "postgres"
     cher.add_recipe "redis"


     chef.add_role "web"
  
  #   # You may also specify custom JSON attributes:
  #   chef.json = { :mysql_password => "foo" }
  end


end
