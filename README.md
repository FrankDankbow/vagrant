# Vagrant

## Assumptions

This assumes that Virtualbox is installed and the extension pack has been installed with your computer rebooted as well.

## AMD64 Machines (Most Machines)

Use the amd64 folders when running Vagrant.

## ARM64 Machines (M-Series Macbooks)

Use the arm64 folders when running Vagrant.

## Vagrant

Install Vagrant for your operating system here: https://developer.hashicorp.com/vagrant/downloads

What is Vagrant and how to use it? https://www.youtube.com/watch?v=sr9pUpSAexE&t=168s

### Vagrant Commands

https://developer.hashicorp.com/vagrant/docs/cli

## Deploying the VM Lab

Clone/Download repo to local file system.

Navigate to which VM folder and architecture you are wanting to build (ex. cd rocky9/arm64)

In Powershell, Bash, or Zsh... run ```vagrant init``` once in the folder that contains the Vagrantfile.

Once that finishes, run ```vagrant up``` and wait for a few minutes (it might take a while). This will stand up the VM / lab environment. If asked about allowing Virtualbox to manage networks, select Allow.

**Important:** You will need to be in the correct, initialized folder for any of these Vagrant commands to control the CPS environment, including to ssh to a machine.

<img src="./assets/vagrant_up.svg" width="100%" height="100%"/>

## Using the environment

Once built, you can access the environment from Virtualbox, or by typing ```vagrant ssh```. If you have a multi-machine environment, this will be followed by the machine name.


<img src="./assets/vagrant_ssh.svg" width="100%" height="100%"/>


## Stopping and Destroying

To simple stop the environment at once, run ```vagrant halt```. The environment can be started again by running ```vagrant up```.

To completely destroy the environment, run ```vagrant destroy```.

All of the vagrant commands must be ran from the folder with your Vagrantfile in it.

<img src="./assets/vagrant_destroy.svg" width="100%" height="100%"/>

## Known Issues/Bugs

I will be updating this section as I find/hear about bugs students have.


#### Mostly Windows Issue

If you run ```vagrant destroy``` and then ```vagrant up``` and get an error along the lines of "Cannot rename folder_XX to folder_YY" then find where Virtualbox stores your VM folders (should be under user home folder) and delete the folders for the VMs that you are trying to build if they were built before. 

After doing so, you can rerun ```vagrant up```.
