# Vagrant & Ansible Collection for Windows Development

## Usage

- Initialized for vagrant if no .vagrant dir

    `vagrant init`

- Set new VBox name (vb.name in vbox section of Vagrantfile)
- Create the VBox and invoke Ansible afterwards

    `VAGRANT_DEFAULT_PROVIDER=virtualbox vagrant up`

- Create the VBox _without_ Ansible provisioner
 
    `VAGRANT_DEFAULT_PROVIDER=virtualbox vagrant up --no-provision`
