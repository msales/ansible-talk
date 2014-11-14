Ansible introducrion at Barcamp Karlsruhe 2014 - https://barcamp-karlsruhe.tixxt.com

Speaker:
David Heidt
david@heidt.biz
http://heidt.biz
@witsches


Slides (in german):
https://speakerdeck.com/witsches/cloud-orchestration-mit-ansible

----

sample commands: 

	# ad-hoc commands:
	ansible -i ec2.py tag_role_webworker --list-hosts
	ansible -i ec2.py all -m ping
	ansible -i ec2.py tag_role_webworker -a "php -v"

	# see what a host has to offer:
	ansible -i ec2.py -u ubuntu tag_Name_redis -m setup

	#simple playbook
	ansible-playbook -i ec2.py redis.yml
	# verify redis setup:
	ansible -i ec2.py -u ubuntu tag_Name_redis -a "redis-cli -a foobar INFO"

	#advanced playbook
	ansible-playbook -i ec2.py nginx-site.yml

