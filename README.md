# Introduction

Simple Beat module to monitor a server with ELK

# Usage

```yaml
---
- hosts: logs
  become: yes
  remote_user: admin
  vars:
    elastic_output_url: logs01:9200,logs02:9200,logs03:9200
    filebeat_enable_modules:
      - system
      - iptables
    filebeat_disable_modules:
      - imperva
  roles:
    - logagent
```
