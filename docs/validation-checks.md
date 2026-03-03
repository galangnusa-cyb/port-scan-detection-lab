# Validation Checks

## Suricata rules loaded
sudo suricata -T -c /etc/suricata/suricata.yaml -v

## EVE JSON has flow events
sudo tail -n 500 /var/log/suricata/eve.json | grep '"event_type":"flow"' | tail
