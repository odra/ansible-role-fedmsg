## Ansible Role: fedmsg
This fedmsg role is used in the CentOS Infra.

It surely depends (see dependencies below) on some other roles.

See also [ansible-infra-playbooks](https://github.com/CentOS/ansible-infra-playbooks) directory to see how the tree/structure is organized

### Variables

Variables are defined at [defaults/main.yml](defaults/main.yml)

```yaml
fedmsg_hub_bin: fedmsg hub executable, defaults to "/usr/bin/fedmsg-hub" 
fedmsg_env: fedmsg mode, should be either "dev" or "prod"
fedmsg_log_level: fedmsg log level, defaulta to "INFO"
fedmsg_hub_memory_limit_mb: Limit max RAM usage for fedmsg-hub, 0 means no limit
fedmsg_hub_auto_restart: boolean flag that autorestart fedmsg in case of failure
fedmsg_enable_websocket_server: boolean flag to enable/disable fedmdg web socket server
fedmsg_websocket_port: fedmsg web socket port to be used, if enabled
fedmsg_status_directory: directory for fedmsg to write its last processed message
fedmsg_post_init_sleep: the number of seconds fedmsg should sleep after initialization
``` 

### Dependencies
This role can depend on some other roles, either statically defined, or dynamically included/imported:
  * See [meta/main.yml](meta/main.yml)
  * Or each <task>.yml under tasks folder for included/imported roles

All those roles are declared in our [requirements.yml](https://github.com/CentOS/ansible-infra-playbooks/blob/master/requirements-production.yml) file.

### License
MIT (see [LICENSE](LICENSE) file)

