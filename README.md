README
======

This project allows you to manage a multi-site Wordpress server.  You can use it to easily create/delete Wordpress sites using Ansible.


Please these files on the Webserver
* /etc/apache2apache2.conf
* /home/ubuntu/create.sql.orig (you can put this anywhere as long as you update the path in wp_create file)
* /home/ubuntu/wp_create (you can put this anywhere as long as you update the path in main.yml)
* /home/ubuntu/wp_delete (you can put this anywhere as long as you update the path in main.yml)


Place these files on the Ansible server
* /etc/ansible/hosts
* /etc/ansible/roles/common/tasks/main.yml (paths for wp_create and wp_delete must match the paths above)
* /etc/ansible/site.yml
* /etc/ansible/wordpress.yml


To run the Ansible playbook:
* $ ansible-playbook -i /etc/ansible/hosts /etc/ansible/site.yml
