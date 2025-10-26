# MPLS BGP VPN (Standard)

![Topology](./images/topology.jpg)

## Summary

Standard MPLS L3VPN configuration with PE-CE BGP routing. Two customer sites with different AS numbers (AS 65000 and AS 65002) communicate through ISP MPLS backbone using VRF isolation and MP-BGP VPNv4.

## Configs

- [CE1.cfg](./configs/CE1.cfg) - Customer Edge 1 (AS 65000)
- [PE1.cfg](./configs/PE1.cfg) - Provider Edge 1 (VRF + MP-BGP + MPLS)
- [PE2.cfg](./configs/PE2.cfg) - Provider Edge 2 (VRF + MP-BGP + MPLS)
- [CE2.cfg](./configs/CE2.cfg) - Customer Edge 2 (AS 65002)

## Verification

```
show ip bgp vpnv4 vrf ISP_A
show mpls forwarding-table
ping vrf ISP_A 192.168.2.1 source 192.168.1.1
```

**Blog:** [Medium Article](link)
