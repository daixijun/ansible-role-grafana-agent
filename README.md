# grafana_agent

Install grafana-agent(https://github.com/grafana/agent)

## Requirements

- Python 3.9+
- Ansible 2.12+

## Role Variables

- **grafana_agent_version**: 0.31.3
- **grafana_agent_download_url**: https://github.com/grafana/agent/releases/download/v{{ grafana_agent_version }}/grafana-agent-linux-amd64.zip
- **grafana_agent_checksum**: https://github.com/grafana/agent/releases/download/v{{ grafana_agent_version }}/SHA256SUMS
- **grafana_agent_checksum_algorithm**: sha256
- **grafana_agent_wal_directory**: /var/lib/grafana-agent
- **grafana_agent_config_file**: /etc/grafana-agent/config.yaml
- **grafana_agent_systemd_unit_file**: /etc/systemd/system/grafana-agent.service
- **grafana_agent_user**: grafana-agent
- **grafana_agent_group**: grafana-agent
- **grafana_agent_server_http_address**: 127.0.0.1:12345

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

MIT

## Author Information

- Xijun Dai <daixijun1990@gmail.com>
