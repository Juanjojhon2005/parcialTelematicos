Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"

  # -------------------------
  # DNS MAESTRO
  # -------------------------
  config.vm.define "maestro" do |maestro|
    maestro.vm.hostname = "maestro.empresa.local"
    maestro.vm.network "private_network", ip: "192.168.56.10"

    maestro.vm.provider "virtualbox" do |vb|
      vb.name = "DNS-MAESTRO"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  # -------------------------
  # DNS ESCLAVO
  # -------------------------
  config.vm.define "esclavo" do |esclavo|
    esclavo.vm.hostname = "esclavo.empresa.local"
    esclavo.vm.network "private_network", ip: "192.168.56.11"

    esclavo.vm.provider "virtualbox" do |vb|
      vb.name = "DNS-ESCLAVO"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  # -------------------------
  # CLIENTE
  # -------------------------
  config.vm.define "cliente" do |cliente|
    cliente.vm.hostname = "cliente.empresa.local"
    cliente.vm.network "private_network", ip: "192.168.56.12"

    cliente.vm.provider "virtualbox" do |vb|
      vb.name = "CLIENTE-DNS"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

end
