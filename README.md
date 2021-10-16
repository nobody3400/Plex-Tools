# Plex-Tools
Plex - Monitoring and Stats
Monitoring of PLEX application using zabbix or graphane.


# Requirements for zabbix version:
- Plex Media server (linux)
- Zabbix 5.4+
- Vnstat
- 
# Requirements with grafana version:
- Plex Media server (linux)
- Zabbix 5.4+
- Grafana
- GeoLite2 Free Geolocation Data (for maps)
- Python 3.6.7+
- Python3-pip
- InfluxDB 1.8.x
- Tautulli - A Python based monitoring and tracking tool for Plex Media Server.
- Varken

# Key Features
- Zabbix Agent (Active)
- Bandwidth by Day/Month/All Time
- Bandwidth by Receive/Transmit/Total
- Graphs For each Day/Month/All Time per Receive/Transmit/Total/Stacked
- Triggers


# Install 
apt-get update
apt-get install vnstat
service vnstat restart
service zabbix-agent restart

#Import Template
Import the plex-tools.yaml template into Zabbix.


# Last Update
October 16, 2021

# Contact
Twitter: @KRelkci
Github: @nobody3400

# Special Thanks
- 
