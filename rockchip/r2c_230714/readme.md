# Add ipv6helper to support IPv6.

For non-bridged modem (dial on modem), modify /etc/config/dhcp to relay ipv6

```
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
```

# Add Zerotier
Zerotier is really useful with ipv6 enabled.

refer to below link:

[https://www.youtube.com/watch?v=pa0tkch3lss](https://www.youtube.com/watch?v=pa0tkch3lss)

[https://www.youtube.com/watch?v=5qzYwvotlNg](https://www.youtube.com/watch?v=5qzYwvotlNg)
