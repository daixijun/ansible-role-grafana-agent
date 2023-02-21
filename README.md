# grafana_agent

Install grafana-agent(https://github.com/grafana/agent)

## Requirements

- Python 3.9+
- Ansible 2.12+

## Role Variables

see [defaults/main.yml](./defaults/main.yml)

## Dependencies

None

## Example Playbook

Install role

```shell
$ ansible-galaxy role install daixijun.grafana_agent
```

```yaml
- hosts: servers
  tasks:
    - name: Include daixijun.grafana_agent
      ansible.builtin.include_role:
        name: daixijun.grafana_agent
      vars:
        grafana_agent_version: 0.31.3
```

## License

[MIT](./LICENSE)

## Author Information

- Xijun Dai <daixijun1990@gmail.com>
