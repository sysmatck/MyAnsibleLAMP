Building a nice LAMP stack and deploying a webserver using Ansible Playbooks.
-------------------------------------------

These playbooks have been built based on the official Ansible examples available at
https://github.com/ansible/ansible-examples, and as the original document
`This repository contains examples and best practices for building Ansible Playbooks`.
But I am learning, so expect not so polished solutions, be aware of the risk of using it...

These playbooks require Ansible 2.2+ and have been designed to use on Ubuntu 16.04
Feel free to tailor it for your system...

This LAMP stack can be on a single node or multiple nodes. The inventory file
'hosts' defines the nodes in which the stacks should be configured.

        [webservers]
        localhost

        [dbservers]
        bensible

Here the webserver would be configured on the local host and the dbserver on a
server called "bensible". The stack can be deployed using the following
command:

        ansible-playbook -i hosts site.yml

Once done, you can check the results by browsing to http://localhost/.
You should see a phpinfo page...
