# fgate-create-address-config
This script accepts a file holding a list of IP addresses (one per line) as an argument & then constructs fortigate address
objects and a group object including all of the address objects.  Objects are named as FILENAME_IPADDRESS and the group is named as FILENAME_Group, so name your file accordingly.  Then the output file named - add_addresses_FILENAME can be used as a script to add the objects to the Fortigate directly.  The input file will accept cidr notation and convert into appropriate net mask (using cidr_to_netmask - stolen from stackoverflow). A lack of cidr notation will be treated as a /32.
