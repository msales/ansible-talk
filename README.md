Ansible introduction at ANSIBLE Meetup Karlsruhe: http://www.meetup.com/de-DE/Ansible-Karlsruhe/

Speaker:
David Heidt
david.heidt@msales.com
http://msales.com
@witsches
@msalestech


Slides:
tba
----

demo commands:

	# ad-hoc commands:
	ansible -i production webworker --list-hosts
	ansible -i production all -m ping
	ansible -i production -u ubuntu webworker -a "lsb_release -a"

	# see what a host has to offer:
	ansible -i production -u ubuntu redis -m setup
  
  # limited command
  ansible -i production -u ubuntu -s loadbalancer -m apt -a "name=nginx state=installed update_cache=true"

	# see what a host has to offer:
	ansible -i production -u ubuntu redis -m setup

	#simple playbook
	ansible-playbook -i production redis.yml

	# verify redis setup:
	ansible -i production redis -a "redis-cli -a foobar INFO"

	#advanced playbook
	ansible-playbook -i production nginx-site.yml

