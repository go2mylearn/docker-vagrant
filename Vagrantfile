# 1
PROVIDER = "vmware_desktop"
BOX_BASE = "centos/7"
VM_RAM = "2048"
VM_CPU = "2"
VM_HOSTNAME = "docker"

Vagrant.configure("2") do |config|
  config.vm.define "docker" do |docker|
    docker.vm.box = BOX_BASE
    docker.vm.hostname = VM_HOSTNAME
    docker.vm.provider PROVIDER do |vm|
      vm.vmx["memsize"] = VM_RAM
      vm.vmx["numvcpus"] = VM_CPU
      vm.gui = true
    end
    docker.vm.provision "shell", path: "install-docker.sh"
  end
end
