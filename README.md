Zabbix-agent Role for Zabbix 3.2
=================

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	# Zabbix server to connect to
	zabbix_agent_server: localhost
	# Zabbix port in the server to connect to
	zabbix_agent_server_port: 10051
	# HostMetadata value in the agent config
	zabbix_agent_metadata: system.uname
	# Prefix to be added to the Hostname value in the agent config
	zabbix_agent_hostname_prefix: ""


Example Playbook
----------------

```
---
- hosts: zabbix-clients
  roles:
       - { role: zabbix-agent, zabbix_agent_server: zabbix.domain.local }
```

License
-------

Apache Licence v2

http://www.apache.org/licenses/LICENSE-2.0

Based on INDIGO project work:

https://github.com/indigo-dc/ansible-role-zabbix-agent