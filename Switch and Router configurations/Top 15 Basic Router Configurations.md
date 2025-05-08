![Router config via console](https://github.com/cyb3rv1k1ng/CCNA-LABS/blob/main/Switch%20and%20Router%20configurations/Router%20config%20via%20console.png)

- Configure Hostname and banner motd
```
Router(config)#host R1-CCNA
R1-CCNA(config)#banner motd #CCNA LABS#
```

-  Enable password
```
R1-CCNA(config)#enable password cisco
```

- Enable line console and line vty password, exec timeout and logging
```
R1-CCNA(config)#line console 0
R1-CCNA(config-line)#password cisco
R1-CCNA(config-line)#exec-timeout 4 0
R1-CCNA(config-line)#logging synchronous

R1-CCNA(config-line)#exit
R1-CCNA(config)#line vty 0 15
R1-CCNA(config-line)#password ccna
R1-CCNA(config-line)#exec-timeout 2 0
R1-CCNA(config-line)#logging synchronous
```

- Disable IP domain lookup and set IP domain name
```
R1-CCNA(config)#no ip domain-lookup
R1-CCNA(config)#ip domain-name cisco.com
```

- Set username and password
```
R1-CCNA(config)#username Admin password cisco
```

- Encrypt all passwords
```
R1-CCNA(config)#service password-encryption
```

- Set current clock time
```
R1-CCNA(config)#clock set 17:15:22 March 29 2025
```

- Set management IP address
```
R1-CCNA(config)#int vlan 1
R1-CCNA(config-if)#no shut
R1-CCNA(config-if)#ip addr 192.168.10.254 255.255.255.0
```

- Save startup config and view startup config
```
R1-CCNA(config)#do write

[OK]
```

