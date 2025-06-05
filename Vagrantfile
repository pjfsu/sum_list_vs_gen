Vagrant.configure("2") do |config|
  (1..2).each do |i|
    config.vm.define "debian_vm#{i}" do |vm|
      vm.vm.box = "debian/bookworm64"
      vm.vm.provider "libvirt" do |libvirt|
        libvirt.memory = 2048
        libvirt.cpus = 2
      end
      vm.vm.hostname = "bookworm#{i}"
      vm.vm.synced_folder ".", "/vagrant", disabled: true
    end
  end
end

