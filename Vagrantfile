# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "varnishtraining"
  config.vm.box_url = "http://download.feryn.eu/varnishtraining.box"
  config.vm.host_name = "varnishtraining"
  config.vm.customize [
        "modifyvm", :id,
        "--name", "Varnish Training",
        "--memory", "1024"
  ]
  config.vm.network :hostonly, "10.10.10.6"
  config.vm.share_folder "v-data", "/home/data", "./", :nfs => true
end
