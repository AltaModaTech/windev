# Journal

## How To Create a New Win Dev Env

### Creating from ISO

- Create the VM using a recent Windows ISO
- Installer
  'I don't have a license'
  'Win10 Pro N for Workstations'
- Initial config
  - Admin user vagrant/vagrant

- Jump to 'Modify the VM' below

### Creating from Vagrant Box
- Get the latest .box
 
  `vagrant box update --box gusztavvargadr/windows-10`

- Prepare for Vagrant
  - Create new folder for the Vagrantfile
    - Name based on month & year, e.g., Win10Aug23
    - Copy previous Vagrantfile to this new folder
    - Edit Vagrantfile
      - 'config.vm.hostname' to match the folder name convention
- Have Vagrant create the VM
  
  `vagrant up` or `vagrant up --no-provision`

### Modify the VM

- After VM starts
  - Rename guest VM appro'ly
- Shutdown VM
  - Change network to bridged over a host NIC
- Start VM
- Accept network discovery
- If created from ISO
  - Enable OpenSSH Server
    - https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=powershell

### Auto install & config

- Update guest VM hostname in Ansible inventory (../playbook/inventory)
- Ansible-playbook

  `ANSIBLE_HOST_KEY_CHECKING=false ansible-playbook ../windev/playbooks/main.yml -i ../windev/playbooks/inventory`

### Manual configs

- Install Winget using Store app
- Install VBox Guest Additions
- Start and config procexp
- Clean up task bar (rm Store, Mail, etc.)

## History

### 06/06/2023

- Created amt/Vagrantfile to manage creating a Windows 10 VM in VirtualBox

### 08/23/2023

- Added How To section at top
- 

## TODO
- VM config
  - bidi clipboard
- After VM is running
  - Install winget
  - Use winget to install
  - Install Gists
    - Devtools
    - Browsers


- Other
  - When to create user & change vagrant's pswd?