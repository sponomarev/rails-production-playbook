Vagrant.configure(2) do |config|
  config.vm.box = 'isiton/centos'

  config.ssh.forward_agent = true
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.define 'application' do |application|
    application.vm.hostname = 'application'
    application.vm.network :private_network, ip: "192.168.15.10"
  end

  config.vm.define 'database' do |database|
    database.vm.hostname = 'database'
    database.vm.network :private_network, ip: "192.168.15.11"
  end
end
