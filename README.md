This is a playbook to setup a Kubernets cluster (one master, one worker node).

The two VMs (Ubuntu 16.04) are created with Vagrant (https://www.vagrantup.com/downloads.html) using Virtualbox provider and the following routine:


```
cd k8s-master
vagrant up
cd ../k8s-worker
vagrant up
```

To run the installation playbook:

```ansible-playbook -i hosts -u vagrant -b --private-key=~/.vagrant.d/insecure_private_key playbook.yml```
