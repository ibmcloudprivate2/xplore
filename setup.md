
# Setup IBM Cloud Private Community Edition (ICP CE)

To setup ICP CE, you will need the following prerequisite.

## prerequisite
- Virtualbox
- Vagrant
- Git

## Virtualbox setup

## Vagrant Setup

## Git Setup

## ICP CE Setup
```
git clone https://github.com/IBM/deploy-ibm-cloud-private.git
cd deploy-ibm-cloud-private
```

**Note**
edit the Vagrantfile and change the CPU from 4 to 3.

From the command prompt, run
```
vagrant up
```
More information about the ICP setup above can be found [here](https://github.com/IBM/deploy-ibm-cloud-private/blob/master/docs/deploy-vagrant.md).


## Access the ICP Dashboard
When the installation is completed, you can access the ICP Dashboard from a browser
```
[ICP Dashboard](https://192.168.27.100:8443/console/)
```

## create a namespace
From the Menu/Admin/Namespaces, create a namespace 'demo'

## Useful Vagrant commands

### ssh into master
In order to continue the tutorial you will need to login to VM.
```
vagrant ssh
```

### Suspend the ICP VM
```
vagrant suspend
```

### Resume the ICP VM
```
vagrant resume
```
