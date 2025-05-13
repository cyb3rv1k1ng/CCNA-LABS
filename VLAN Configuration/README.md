---
tags:
  - networking
  - CCNA
date created: 2025-03-23
---
![[Pasted image 20250323084038.png]]

```
Switch(config)#host S0
S0(config)#int range fa0/1
S0(config-if-range)#sw mode acc
S0(config-if-range)#sw acc vlan 10
S0(config-if-range)#exit

S0(config)#int fa1/1
S0(config-if)#sw mode acc

S0(config-if)#int fa3/1
S0(config-if)#sw mode acc
S0(config-if)#sw acc vlan 10

S0(config-if)#int fa2/1
S0(config-if)#sw mode acc
S0(config-if)#sw acc vlan 10

S0(config-if)#int fa6/1
S0(config-if)#sw mode acc
S0(config-if)#sw acc vlan 30

S0(config-if)#int fa7/1
S0(config-if)#sw mode acc
S0(config-if)#sw acc vlan 30

S0(config-if)#int fa3/1
S0(config-if)#sw acc vlan 20

S0(config-if)#int fa2/1
S0(config-if)#sw acc vlan 20
S0(config-if)#exit

S0(config)#do wr
S0(config)#do sh vlan
```

- Switch 1 config:
```
Switch(config)#host S1
S1(config)#int range fa0/1
S1(config-if-range)#sw mode acc
S1(config-if-range)#sw acc vlan 10
S1(config-if-range)#exit

S1(config)#int fa1/1
S1(config-if)#sw mode acc

S1(config-if)#int fa3/1
S1(config-if)#sw mode acc
S1(config-if)#sw acc vlan 10

S1(config-if)#int fa2/1
S1(config-if)#sw mode acc
S1(config-if)#sw acc vlan 10

S1(config-if)#int fa6/1
S1(config-if)#sw mode acc
S1(config-if)#sw acc vlan 30

S1(config-if)#int fa7/1
S1(config-if)#sw mode acc
S1(config-if)#sw acc vlan 30

S1(config-if)#int fa3/1
S1(config-if)#sw acc vlan 20

S1(config-if)#int fa2/1
S1(config-if)#sw acc vlan 20
S1(config-if)#exit

S1(config)#do wr
S1(config)#do sh vlan
```

- Assign IP addresses to all PCs

![[Pasted image 20250323080505.png]]

![[Pasted image 20250323084525.png]]

- Test communication between devices. You will observe communication between devices in different VLANs is fails. PCs that are not in the same VLAN cannot see each other and so don't know how to get to that destination as they are also on different networks. This is where the router comes in.
- As you can see the PCs in `192.168.10.0` network can communicate but when we try to ping the `192.168.20.0` network communication fails.

![[Pasted image 20250323081126.png]]

***
Links to this page

[[VLANs Access and Trunk Links]]

