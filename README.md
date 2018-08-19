## Tomcat Deployment using Ansible

These playbooks will set up the Tomcat 7 in the target machines including dependencies like Java, that are required by 
Tomcat. 

To set up Tomcat in 10 hosts, first put all those hosts in the hosts file. 

And then run the playbook, using this command:

	ansible-playbook -i hosts site.yml

After the process is done, you should be able to see the Tomcat
Application Servers running on the port "8444", on the target machines.

You can see the Tomcat default page at http://ipaddress-of-machine:8444

## Rolling restart of these Tomcat Application servers in those 10 hosts

To start the rolling restart if the tomcat servers, 

Run the playbook, using this command:

        ansible-playbook -i hosts restart.yml

All the machines will restart sequentially one by one.

<b> NOTE:</b>These playbooks are created and tested in AWS. We have to change the remote_user (ec2-user) to that respective user.  
