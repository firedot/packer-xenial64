# packer-xenial64
firedot-xenial64

**This repository is based on [that](https://github.com/nabels-coolblue/packer-xenial64) repository.**

## Used technologies

**Packer** 
You could learn more about packer by visiting: https://www.packer.io/intro/

**VirtualBox** 
You could learn more about VirtualBox by visiting: https://www.virtualbox.org/

**Vagrant**
You could find more about vagrant [here](https://www.vagrantup.com/intro/index.html) 


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

## Vagrant phase

1. Download and install vagrant from [here](https://www.vagrantup.com/downloads.html)

2. You could add your box to Vagrant, run the following command: 

````
vagrant box add --name mybasebox mybasebox.box
````
3. In order to begin working, you will need a Vagrantfile - the file that configures your Vagrant box. 
   * You could create the minimal Vagrantfile required by executing the following command:
  ````
  vagrant init -m boxname
  
  # or download a box from the VagrantCloud:
  
  vagrant init -m username/boxname  

  `````
   * After running the previous command, you will have a file, with the following contents: 
    
  ````
  Vagrant.configure("2") do |config|
  config.vm.box = "boxname"
end
  ````
4 Start your box by typing:
  ````
  vagrant up
  ````
5. You could check if your box is up and running by typing:
  ````
  vagrant status
  ````
  or by connecting to it via SSH: 
  ````
  vagrant ssh
  ````

