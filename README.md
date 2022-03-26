# AnsibleTask
For The Inventory File
i gave name for the host it will be connected to using the playbook (lampstack)
as i don't have a centos machine i used an EC2 instance from aws 
so i added the credentials for accessing the EC2
which is the host name (DNS Name) of the EC2 instnace
then the username for the EC2 instance (ec2-user)
and the port it will be accessed through which is 22 for ssh
and the last this the private key to access the instance

(sorry i will terminate the instance that's why i will not upload the key file xD)

For The Playbook File
i specified the host it will run those task on from the inventory file (lampstack)
and as i will install some packages i can't do that as a normal user
so i will connect remotely by the root user
and then specified the variables for the packages that will be installed
and the variables list for the enable and starting the service (because they have different names from the package itself)
and the last variable list for ports that will be enabled on the host
then i looped over the variables on the tasks section 
after that i added the php file 
and permit the ports on the firewall
last thing is testing the php file is actually hosted right

(for me i don't know what was the issue with the instance 
it performed all the tasks well but when i connect to it using it's public ip it fails
although i made sure that the routing table is public (0.0.0.0)
and the security groups too having the http and https permission 
so i couldn't test that the php file is hosted well
but for the tasks it's worked well)

