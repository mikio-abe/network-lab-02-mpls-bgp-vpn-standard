# Verification Commands

## VRF
Check VRF configuration and routing table
```
show ip vrf
show ip route vrf ISP_A
```

## MP-BGP
Check VPNv4 route exchange
```
show ip bgp vpnv4 all summary
show ip bgp vpnv4 vrf ISP_A
show ip bgp vpnv4 vrf ISP_A 192.168.2.0
```

## MPLS
Check LDP neighbor and label forwarding
```
show mpls ldp neighbor
show mpls forwarding-table
show mpls forwarding-table vrf ISP_A
```

## PE-CE BGP
Check BGP neighbor with CE routers
```
show ip bgp summary
show ip bgp vrf ISP_A summary
show ip bgp vrf ISP_A neighbors
```

## Connectivity
Test end-to-end connectivity
```
ping vrf ISP_A 192.168.2.1 source 192.168.1.1
traceroute vrf ISP_A 192.168.2.1 source 192.168.1.1
```
