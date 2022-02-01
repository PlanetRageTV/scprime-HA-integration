# scprime-HA-integration
Home Assistant Integration for Monitoring SCPrime Servers

With the help of the pre-configured RESTful Sensors in the sensors.yaml File you can gather information about your (or any) SCPrime Host that is announced without the need of any edits or alterations to your host.

The Information is gathered using the RESTful API from Siacentral.com.

Please not that within the sensors.yaml you have to change [SCPRIMEHOSTIP] for your hosts IP or DDNS Name with which it is announced (no local IPs!).

To integrate the sensors to your home assistant installation simply upload the sensors.yaml to the same folder as your configuration.yaml is in your home assistant installation.
Then you need to load the custom sensors within your configuration.yaml.

In order to load the custom sensors, open your configuration.yaml file and add:

sensor: !include sensors.yaml

at the end. Then check / reload configuration for the sensors to be loaded.

Currently the sensor refreshes the data every 600 seconds (10 Minutes), to change that simply edit the scan_interval in the sensors.yaml. The value is in seconds.

Use this integration on your own risk, I am not responsible for any problems or errors or if your house explodes.

Have fun!

#The following Sensors are created
"SCP Host Address" - Address the host is announced with

"SCP Host Version" - Currently running version of the SCPrime Daemon on the host

"SCP Host Uptime" - Reported Uptime Value

"SCP Host Online" - Boolean if host is online

"SCP Host Total Storage TB" - Total Host Storage in TB (decimal!)
 
"SCP Host Used Storage GB" - Used Host Storage in GB (decimal!)

"SCP Host Blockheight" - Host reported Blockheight

"SCP Host Online Since" - First host announcement.

"SCP Exchange Rate USD" - Current exchange Rate of SCPrimecoin to USD
