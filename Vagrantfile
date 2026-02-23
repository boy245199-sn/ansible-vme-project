Vagrant.configure("2") do |config|
  # Utiliser Ubuntu 20.04 comme base
  config.vm.box = "ubuntu/focal64"

  # Configuration matérielle commune (1 Go RAM, 1 CPU)
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
  end

  # VM pour la base de données
  config.vm.define "db" do |db|
    db.vm.hostname = "db"
    db.vm.network "private_network", ip: "192.168.33.11"
  end

  # VM pour le serveur web
  config.vm.define "web" do |web|
    web.vm.hostname = "web"
    web.vm.network "private_network", ip: "192.168.33.12"
  end

  # VM pour le partage de fichiers
  config.vm.define "files" do |files|
    files.vm.hostname = "files"
    files.vm.network "private_network", ip: "192.168.33.13"
  end

  # VM pour le monitoring
  config.vm.define "monitor" do |monitor|
    monitor.vm.hostname = "monitor"
    monitor.vm.network "private_network", ip: "192.168.33.14"
  end
end