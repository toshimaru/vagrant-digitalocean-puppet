Vagrant.configure('2') do |config|
  config.vm.provision "shell", inline: "rpm -Uvh http://ftp-srv2.kddilabs.jp/Linux/distributions/fedora/epel/6/x86_64/epel-release-6-8.noarch.rpm --force"
  config.vm.provision "shell", inline: "yum -y install puppet"

  config.vm.provider :digital_ocean do |provider, override|
    override.ssh.private_key_path = '~/.ssh/id_rsa'
    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"

    provider.client_id = '{your_client_id}'
    provider.api_key = '{your_api_key}'

    provider.image                = 'CentOS 6.4 x64'
    provider.region               = 'San Francisco 1'
    provider.size                 = '512MB'
  end

  config.vm.provision "puppet" do |puppet|
    puppet.options                = "--verbose"
  end
end
