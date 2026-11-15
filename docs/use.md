# Import and use a template

## Import

1. Download the template file from the repository: one `.yaml` file in each
   template directory.
2. In Zabbix 6.0, open **Configuration → Templates → Import** and choose the file.
3. Link the template to a host that has an SNMP interface (SNMPv2) for the NAS.

## Macros

Change a threshold on the host, not in the template. The defaults:

| Template | Macro | Default | Meaning |
|---|---|---|---|
| QNAP | `{$CPU_TEMPERATURE_ALARM}` | 65 | CPU temperature in degrees C |
| QNAP | `{$DISK_LATENCY_ALARM}` | 30 | Disk latency in ms |
| QNAP | `{$HDD_TEMPERATURE_ALARM}` | 50 | Disk temperature in degrees C |
| QNAP | `{$POOL_SIZE_ALARM}` | 15 | Pool size alarm in % |
| Synology | `{$DISK_UTIL_WARN}` | 80 | Disk utilisation warning in % |
| Synology | `{$DISK_UTIL_HIGH}` | 90 | Disk utilisation high in % |

## What each template contains

Each template directory has a README with the full list of discovery rules,
items and triggers:

- [QNAP SNMPv2 (6.0)](https://github.com/DotifyBIZ/zabbix-templates/blob/main/QNAP%20SNMPv2%20(6.0)/README.md)
- [Synology DiskStation SNMPv2 (6.0)](https://github.com/DotifyBIZ/zabbix-templates/blob/main/Synology%20DiskStation%20SNMPv2%20(6.0)/README.md)
