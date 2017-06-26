Simple zabbix-agent Role for Zabbix 3.2
=======================================

Role for Zabbix 3.2 for most popular linux distros with easy and minimal configuration.

Supported OSes
--------------
Debian 7 and 8  
Ubuntu LTS 16 and (not tested) 14
RHEL / CentOS 6, 7 and (not tested) 5

May support more OSes, please report any success/failures.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	# Zabbix server to connect to
	zabbix_agent_server: localhost
	# Zabbix port in the server to connect to
	zabbix_agent_server_port: 10051

How to Install
--------------

```
cd /etc/ansible/roles
git clone https://github.com/varnav/ansible-zabbix-3.2-agent.git zabbix-agent 
```

or

```
cd /etc/ansible/roles
ansible-galaxy install varnav.zabbix-3.2-agent
```


Example Playbook
----------------

```
---
- hosts: zabbix-clients
  roles:
       - { role: zabbix-agent, zabbix_agent_server: zabbix.domain.local }
```

How to run
----------

``` 
ansible-playbook zabbix-agent.yml --limit zabbix-clients 
```

License
-------

Apache Licence v2

http://www.apache.org/licenses/LICENSE-2.0

Based on INDIGO project work:

https://github.com/indigo-dc/ansible-role-zabbix-agent
