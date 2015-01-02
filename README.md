Simple Development Bootstrap for Node.js

## Pre-requisites

Vagrant: https://www.vagrantup.com

Virtual Box: https://www.virtualbox.org/

Chef Development Kit: https://downloads.chef.io/chef-dk/

Vagrant Omnibus Plugin

	vagrant plugin install vagrant-omnibus	

Vagrant Berkshelf Plugin

	vagrant plugin install vagrant-berkshelf


## Setup

Clone Repo

	git clone https://github.com/AdamPrendergast/vagrant-nodejs-bootstrap.git project_name

Run Vagrant Up

    cd project_name
  	vagrant up

Run Node Server

    vagrant ssh
    cd /vagrant/app
    node server.js
