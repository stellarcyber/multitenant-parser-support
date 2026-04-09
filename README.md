# multitenant-parser-support
syslog-ng configurations to support multitenant mapping

Stellar multitenancy can be supported through syslog-ng that has a lookup mechanism
which utilizes a simple csv file for mapping a value to the stellar tenant. 

Syslog-ng then is used to create a json object with all the relevant pieces needed for the stellar log forwarder
to route to the correct parser. The json object includes the vendor, product, format, originating host, the stellar tenant id, and the raw message.

More information can be found here:
https://docs.stellarcyber.ai/6.4.x/Configure/LogParser/Ingesting-multi-tenant.htm

## Sample configs
There are several sample config files provided
- fg-multitenant.conf:  fortigate example which maps VDOM to stellar tenant id using the vdom_mapping.csv
- fg-devid-multitenant.conf:  fortigate example which maps a devices SERIAL NUMBER to stellar tenant id using the fg_mapping.csv
- pan-multitenant.conf:  palo-alto firewall example which maps SERIAL NUMBER to stellar tenant id using the sn_mapping.csv

