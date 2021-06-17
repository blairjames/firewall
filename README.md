# firewall
- Simple configuration file style wrapper for iptables. Provides the option to run firewall as a systemd service.
- Clone into /opt directory please.

# To run as a once off script to update the local firewall
- sudo /opt/firewall/firewall.conf

# To run the firewall as a systemd service 
- copy the unit file "firewall_service" to "/etc/systemd/system/"
- execute: 
- "sudo systemctl daemon-reload && sudo systemctl restart firewall && sudo systemctl enable firewall && sudo systemctl status firewall"
- The firewall can now be controlled using the standard systemd controls. 
- To reinitialise after modifying rules: "sudo systemctl restart firewall" 

# To view logs
- Following: "sudo journalctl -ef | grep IPTABLES"
- Static: "sudo journalctl -e | grep IPTABLES"
