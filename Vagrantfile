# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

# Percona XtraDB Cluster (192.168.33.70)
  config.vm.define "xdb1" do |xdb1|
    xdb1.vm.box = "debian/stretch64"
    xdb1.vm.hostname = "xdb1"
    xdb1.vm.network "private_network", ip: "192.168.33.71"
  end

  config.vm.define "xdb2" do |xdb2|
    xdb2.vm.box = "debian/stretch64"
    xdb2.vm.hostname = "xdb2"
    xdb2.vm.network "private_network", ip: "192.168.33.72"
  end

  config.vm.define "xdb3" do |xdb3|
    xdb3.vm.box = "debian/stretch64"
    xdb3.vm.hostname = "xdb3"
    xdb3.vm.network "private_network", ip: "192.168.33.73"
  end

# DWH M-M replication
  config.vm.define "dwh1" do |dwh1|
    dwh1.vm.box = "debian/stretch64"
    dwh1.vm.hostname = "dwh1"
    dwh1.vm.network "private_network", ip: "192.168.33.81"
  end

  config.vm.define "dwh2" do |dwh2|
    dwh2.vm.box = "debian/stretch64"
    dwh2.vm.hostname = "dwh2"
    dwh2.vm.network "private_network", ip: "192.168.33.82"
  end

# Zabbix 4.0
  config.vm.define "zbx" do |zbx|
    zbx.vm.box = "debian/stretch64"
    zbx.vm.hostname = "zbx"
    zbx.vm.network "private_network", ip: "192.168.33.80"
    zbx.vm.network "forwarded_port", guest: 80, host: 8080
  end

end