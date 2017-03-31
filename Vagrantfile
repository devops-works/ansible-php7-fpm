Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provider "virtualbox" do |v|
    v.linked_clone = true
  end

  config.vm.define "php7" do |php7|
  end

  config.vm.provision "shell",
    :path => "vagrant_specs.sh",
    :upload_path => "/home/ubuntu/specs",
    # change role name below
    :args => "--install ansible-php7-fpm"
end
