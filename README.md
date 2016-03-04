Ansible introduction 
====================
@ ANSIBLE Meetup Karlsruhe: http://www.meetup.com/de-DE/Ansible-Karlsruhe/

Speaker:
David Heidt

david.heidt@msales.com

[http://msales.com](http://msales.com)



[@witsches](https://twitter.com/witsches)


[@msalestech](https://twitter.com/msalestech)


Slides:

http://msales.com/wp-content/uploads/2016/03/introducing-ansible.pdf

Article:

http://msales.com/techblog/ansible-meetup-karlsruhe/


* * *

demo commands:

	# ad-hoc commands:
	ansible -i production webworker --list-hosts
	ansible -i production all -m ping
	ansible -i production -u ubuntu webworker -a "lsb_release -a"

	# see what a host has to offer:
	ansible -i production -u ubuntu redis -m setup

	# limited command
	ansible -i production -u ubuntu -s webworker -m apt -a "name=nginx state=installed update_cache=true" -l

	# see what a host has to offer:
	ansible -i production -u ubuntu redis -m setup

	# simple playbook
	ansible-playbook -i production redis.yml

	# role playbook
	ansible-playbook -i production nginx-site.yml
