# Fluent Bit Ansible Role

Fluent Bit is an open source and multi-platform Log Processor and Forwarder which allows you to collect data / logs from different sources, unify and send them to multiple destinations.

## Installation

``` yaml
# requirments.yaml
- src: git@github.com:RashadAnsari/ansible-role-fluent-bit.git
  scm: git
  version: master
  name: fluent-bit
```

## Role Variables

``` yaml
fluentbit_service_flush_seconds: 5
fluentbit_service_daemon: false
fluentbit_service_log_level: info
fluentbit_service_custom_parsers_file: []
fluentbit_service_enable_metrics: false
fluentbit_service_metrics_listen_ip: 0.0.0.0
fluentbit_service_metrics_listen_port: 2020

fluentbit_custom_conf: []
```

## Example Playbook

``` yaml
- hosts: servers
  roles:
    - fluent-bit
```
