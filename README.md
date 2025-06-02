# Elementary OS Aucix Vagrant Environment

## Overview
This project provides a Vagrant configuration for quickly setting up an Elementary OS development environment. It uses a custom Vagrant box based on Elementary OS with pre-configured settings and installs a set of useful development and productivity tools.

## Requirements
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)
- At least 8GB of RAM available for the VM
- At least 4 CPU cores available for the VM

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/elementary_aucix_vagrant_env.git
   cd elementary_aucix_vagrant_env
   ```

2. Start the Vagrant environment:
   ```
   vagrant up
   ```

   This will:
   - Download the aucix/elementary_aucix box (version 1.2)
   - Configure VirtualBox with 4 CPUs and 8GB RAM
   - Provision the VM with Ansible to install additional software

3. The VM will automatically start with a GUI interface.

## Installed Software

The environment comes with the following software pre-installed:

### Development Tools
- build-essential (compiler and development libraries)
- git (version control)

### System Utilities
- htop (system monitor)
- realpath (path resolution utility)
- gdebi (package installer)
- VirtualBox guest additions

### Applications
- GIMP (image editor)
- LibreOffice (office suite)
- Chromium Browser (web browser)

## Usage

- To start the VM: `vagrant up`
- To stop the VM: `vagrant halt`
- To destroy the VM: `vagrant destroy`
- To SSH into the VM: `vagrant ssh`

## Customization

You can modify the `Vagrantfile` to adjust VM settings such as memory and CPU allocation:

```ruby
config.vm.provider "virtualbox" do |virtualbox|
  virtualbox.gui = true
  virtualbox.cpus = 4        # Change this to allocate more/fewer CPUs
  virtualbox.memory = 8192   # Change this to allocate more/less memory (in MB)
end
```

You can also modify the `playbook.yml` file to install additional packages by adding them to the list.

## License

[Specify the license here]
