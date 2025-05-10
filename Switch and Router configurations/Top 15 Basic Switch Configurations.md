

![switch config via console.png](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/Switch%20and%20Router%20configurations/switch%20config%20via%20console.png)

- Configure Hostname and banner motd
```
Switch(config)#host SW1-CCNA
SW1-CCNA(config)#banner motd #CCNA LAB SWITCH#
```

-  Enable password
```
SW1-CCNA(config)#enable password cisco
SW1-CCNA(config)#line console 0
```

- Enable line console and line vty password, exec timeout and logging
```
SW1-CCNA(config-line)#password cisco
SW1-CCNA(config-line)#login
SW1-CCNA(config-line)#exec-timeout 3 0
SW1-CCNA(config-line)#logging synchronous

SW1-CCNA(config)#line vty 0 15
SW1-CCNA(config-line)#password cisco
SW1-CCNA(config-line)#login
SW1-CCNA(config-line)#exec-timeout 3 0
SW1-CCNA(config-line)#logging synchronous
```

- Disable IP domain lookup and set IP domain name
```
SW1-CCNA(config-line)#no ip domain lookup
SW1-CCNA(config)#ip domain-name cisco.com
```

- Set username and password
```
SW1-CCNA(config)#username Admin password cisco
```

- Encrypt all passwords
```
SW1-CCNA(config)#service password-encryption
```

- Set current clock time
```
SW1-CCNA#clock set 07:03:30 March 23 2025
```

- Set management IP address
```
SW1-CCNA(config)#int vlan 1
SW1-CCNA(config-if)#no shut
SW1-CCNA(config-if)#ip addr 192.168.10.254 255.255.255.0
SW1-CCNA(config)#ip default-gateway 192.168.10.1
```



