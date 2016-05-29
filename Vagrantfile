# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider :virtualbox do |vb|
      vb.name = "app.intranet"
          vb.customize [ 'modifyvm', :id, '--memory', '512' ]
	      vb.customize [ 'modifyvm', :id, '--cpus', '1' ]
	        end

		  config.vm.network :private_network, ip: "192.168.0.11"
		    config.vm.synced_folder "D:\Projects", "/Projects"
		      config.vm.box  = "precise64"
		        config.vm.hostname = "Vagrant-test"

			  config.vm.provision :puppet do |puppet|
			      puppet.manifests_path = "puppet/manifests"
			          puppet.manifest_file = "site.pp"
				      puppet.module_path = "puppet/modules"
				        end


					end
