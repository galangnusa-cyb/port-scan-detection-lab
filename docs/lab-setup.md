# Lab Setup Summary

- Ubuntu has two interfaces; Suricata captures on `ens34` (192.168.28.128).
- Suricata EVE JSON output: `/var/log/suricata/eve.json`
- Splunk Enterprise runs on the same Ubuntu host and monitors `eve.json` with `sourcetype=suricata:eve`.
