# packer-xenial64
firedot-xenial64

**This repository is based on [that](https://github.com/nabels-coolblue/packer-xenial64) repository.**

## Used technologies

**Packer** 
You could learn more about packer by visiting: https://www.packer.io/intro/

**VirtualBox** 
You could learn more about VirtualBox by visiting: https://www.virtualbox.org/

### VirtualBox phase
Install VirtualBox on your machine. 
Instructions on how it's done may be found [here](https://www.virtualbox.org/manual/ch02.html)

### Packer phase
1. Download and install [packer](https://www.packer.io/downloads.html) 
2. Run the following command in the directory where you have cloned the repository:

````
packer build template.json
````
3. You could upload the box created by you during the packer phase to the [VagrantCloud](https://app.vagrantup.com/boxes/search) 
