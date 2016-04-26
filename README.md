Very simple example setup.

Requirements
============

Virtualbox ( http://www.virtualbox.org )
Vagrant ( http://www.vagrantup.com )
Ansible ( brew install ansible )
Git ( er.. )

What do you get?
================

After running this playbook you'll have a local server on 192.168.33.10 with the following:
* Gitlab on port 80/443 (dockerised)
* Cockpit on 9090 ( root / vagrant )
* Firewall setup for these ports
* Fail2ban setup
* Installs Logwatch
* Automatic updates on

This is meant for experimentation; This could set your servers on fire if you're careless, you have been warned.


