|VLAN|Name|Subnet|Gateway|
|---|---|---|---|
|10|Administration|`192.168.10.0/24`|`192.168.10.1`|
|20|Sales|`192.168.20.0/24`|`192.168.20.1`|
|30|IT|`192.168.30.0/24`|`192.168.30.1`|
|40|Internal Servers|`192.168.40.0/24`|`192.168.40.1`|
|50|DMZ|`192.168.50.0/24`|`192.168.50.1`|
|99|Management|`192.168.99.0/24`|`192.168.99.1`|

Important addresses:

- Internal DNS/HTTP server: `192.168.40.10`
    
- DMZ web server: `192.168.50.10`
    
- Switch management addresses: `192.168.99.2`, `.3`, `.4` (verify the assignment for each switch).