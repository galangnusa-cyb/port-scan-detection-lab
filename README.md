# Port Scan Detection Engineering Lab (Suricata + Splunk)

Detect reconnaissance activity by generating multiple Nmap scan types and building behavior-based detections in Splunk using Suricata EVE JSON telemetry.

## Lab Topology
- Kali Linux: attacker/scanner (Nmap)
- Ubuntu Server: target + sensor (Suricata on `ens34`)
- Splunk Enterprise: running on the same Ubuntu host, ingesting `/var/log/suricata/eve.json`

## What this project demonstrates
- Telemetry collection: Suricata EVE JSON (`eve.json`) → Splunk (`sourcetype=suricata:eve`)
- Detection engineering: port sweep & host sweep detections with thresholds to reduce false positives
- Basic SOC artifacts: queries, alert configuration, and a small dashboard

## Reproduce
1. Install and configure Suricata to capture on the correct interface (example: `ens34`)
2. Ensure EVE JSON is enabled: `/var/log/suricata/eve.json`
3. In Splunk, ingest `eve.json` (monitor input) with `sourcetype=suricata:eve`
4. Run scans from Kali and validate detections in Splunk

## Notes
- Add allowlists and throttling to reduce noise for authorized scanners.
