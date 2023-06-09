# Vagrant & Ansible Collection for Windows Development

## Usage

- Set new VBox name (vb.name in vbox section of Vagrantfile)
- Create the VBox and invoke Ansible afterwards

    `vagrant up`

- Create the VBox _without_ Ansible provisioner
 
    `vagrant up --no-provision`
