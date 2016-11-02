# ansible-zabbix-agent

Install zabbix-agent

Works on:
* CentOS 6
* CentOS 7
* Ubuntu trusty
* Ubuntu xenial


## Variables
`zabbix_version: 3.0`

`labbix_log_size: 0`
Max log size in MB, with `0` log rotation is disabled

```
zabbix_servers:
  - 127.0.0.1
```
Zabbix servers and proxies, must be a list

`zabbix_agent_hostname: "{{ inventory_hostname }}"`
Zabbix agent hostname

`zabbix_enable_active: false`
Enable active checks

`zabbix_enable_remote: false`
Allow running remote commands

`zabbix_enable_root: false`
Allow the agent to run as *root*


## Dependencies
- **[ansible-zabbix-repo](https://github.com/aliusmiles/ansible-zabbix-repo)**

## Example Playbook
    - hosts: all
      roles:
        - role: ansible-zabbix-agent
          zabbix_version: 3.0
          zabbix_servers:
            - 127.0.0.1


## License

MIT


## Author Information

Taras Bondarchuk
