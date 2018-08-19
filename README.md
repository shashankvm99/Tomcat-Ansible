## Tomcat Deployment using Ansible

These playbooks will set up the Tomcat 7 machines including dependencies like Java, that are required by 
Tomcat. 

To set up Tomcat in 10 hosts, first put all those hosts in the hosts file. 

And then run the playbook, using this command:

	ansible-playbook -i hosts site.yml

After the process is done, you should be able to see the Tomcat
Application Servers running on the port "8444", on the target machines.

## Rolling restart of these Tomcat Application servers in those 10 hosts

To start the rolling restart if the tomcat servers, 

Run the playbook, using this command:

        ansible-playbook -i hosts restart.yml


