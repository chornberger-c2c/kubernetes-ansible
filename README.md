sed -i /192.168.33/d /home/horni/.ssh/known_hosts

ansible-playbook -i hosts -u vagrant -b --private-key=/home/horni/.vagrant.d/insecure_private_key playbook.yml 
