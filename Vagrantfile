Vagrant::Config.run do |config|

  config.vm.box = "ubuntu-1104-server-i386"
  config.vm.box_url = "http://dl.dropbox.com/u/7490647/talifun-ubuntu-11.04-server-i386.box"

  config.vm.forward_port("web", 3000, 3000)
  config.vm.network("33.33.00.10")
  
  config.vm.share_folder "leap-lite", "/home/vagrant/src/leap-lite", "../leap-lite"

  config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = "cookbooks"
     chef.add_recipe "postgresql"
     chef.add_recipe "redis"
  #   chef.add_role "web"
  #
  #   # You may also specify custom JSON attributes:
  #   chef.json = { :mysql_password => "foo" }
   end

  
end
