# VLAN Configuration

![network topology](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/VLAN%20Configuration/network%20topology.png)



- Switch 1 config: Assign hostname and create VLANs
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

![IP Assignment](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/VLAN%20Configuration/IP%20configuration%201.png)

![IP Assignment](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/VLAN%20Configuration/IP%20configuration%202.png)

- Test communication between devices. You will observe communication between devices in different VLANs is fails. PCs that are not in the same VLAN cannot see each other and so don't know how to get to that destination as they are also on different networks. This is where the router comes in.
- Only PCs in the same VLAN will be able to communicate.

![Test communication](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/VLAN%20Configuration/ping%20test.png)


