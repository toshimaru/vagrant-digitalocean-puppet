##Requirement

* vagrant command
* vagrant-digitalocean plugin

###Intall vagrant-digitalocean plugin

    $ vagrant plugin install vagrant-digitalocean

##Create a droplet on Digital Ocean

    $ git clone https://github.com/toshimaru/vagrant-digitalocean-puppet
    $ cd vagrant-digitalocean-puppet

Add your own `client_id` and `api_key` in `Vagrantfile`.

    $ vagrant up --provider digital_ocean

##See also

* <http://blog.toshimaru.net/digital-ocean-vagrant-puppet/> (Japanese)
