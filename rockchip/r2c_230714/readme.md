# add ipv6helper to support IPv6.

For non-bridged modem (dial on modem), modify /etc/config/dhcp to relay ipv6

··
config dhcp 'lan'
    ......
    option ra 'relay'
    option dhcpv6 'relay'
    option ndp 'relay'
    
config dhcp 'wan6'
    option interface 'wan6'
    option dhcpv6 'relay'
    option ra 'relay'
    option ndp 'relay'
    option master '1'
··
