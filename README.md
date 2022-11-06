# Introduction

Simple Beat module to monitor a server with ELK

# Usage

```yaml
---
- hosts: logs
  become: yes
  remote_user: admin
  vars:
    filebeat_enable_modules:
      - system
      - iptables
    filebeat_disable_modules:
      - imperva
  roles:
    - logagent
```
