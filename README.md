# firewall
Simple conf file style wrapper for iptables. Provides the option to run firewall as a systemd service.

Clone into /opt directory please.

# To run the firewall as a systemd service 
- copy the unit file "firewall_service" to "/etc/systemd/system/"
- execute 
``` "sudo systemctl daemon-reload && sudo systemctl restart firewall && sudo systemctl enable firewall && sudo systemctl status firewall"
```
