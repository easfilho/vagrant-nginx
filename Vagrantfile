Vagrant.configure("2") do |config|
  config.vm.define "ubunt nginx"
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "public_network", bridge: "wlp1s0"
  
  $script = <<-SCRIPT
  sudo apt-get update
  sudo apt-get install nginx -y
  SCRIPT
  config.vm.provision "shell", inline: $script
  
  config.vm.synced_folder ".", "/usr/share/nginx/html/", create: true

end