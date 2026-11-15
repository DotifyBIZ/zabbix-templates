# Zabbix templates

Zabbix 6.0 templates that monitor NAS devices over SNMPv2. There are two:

| Template | Monitors |
|---|---|
| QNAP SNMPv2 (6.0) | QNAP NAS: disks, LUNs, pools, volumes, fans, RAID and network interfaces |
| Synology DiskStation SNMPv2 (6.0) | Synology DiskStation NAS: system, disks, RAID, SMART, services and I/O |

Nothing here runs on its own. A Zabbix administrator imports a template into a
Zabbix server by hand.

- Zabbix administrators: [Import and use a template](use.md)
- The owning team: [Ownership](ownership.md)
- People who change the templates: [Change a template](development.md)
