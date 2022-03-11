Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/impish64"
  config.vm.hostname = "test"
  config.vm.network "forwarded_port", guest: 3000, host: 3000, host_ip: "127.0.0.1", auto_correct: true
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/main.yml"
    ansible.become = true
  end
end
