# Ansible Role: statsd_exporter

## Description

Deploy prometheus [statsd_exporter](https://github.com/prometheus/statsd_exporter) using ansible.

## Requirements

- Ansible >= 2.7 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `statsd_exporter_version` | 0.4.0 | statsd_exporter package version |
| `statsd_exporter_web_listen_address` | "0.0.0.0:9102" | Address on which statsd_exporter will listen |
| `statsd_exporter_config_flags_extra` | {} | Additional configuration flags passed at startup to statsd_exporter binary |

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - statsd_exporter
```
