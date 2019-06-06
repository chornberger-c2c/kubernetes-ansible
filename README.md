This is a playbook to setup a Kubernets cluster (one master, one worker node).

The two VMs (Ubuntu 16.04) are created with Vagrant using Virtualbox provider and the following routine:


```
mkdir -p k8s-master
mkdir -p k8s-worker
cp -a Vagrantfile k8s-master
cp -a Vagrantfile.2 k8s-worker/Vagrantfile
cd k8s-master
vagrant up
cd ../k8s-worker
vagrant up
```

To run the installation playbook:

```ansible-playbook -i hosts -u vagrant -b --private-key=~/.vagrant.d/insecure_private_key playbook.yml```
