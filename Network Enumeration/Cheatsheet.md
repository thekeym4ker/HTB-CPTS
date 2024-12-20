# Host Discovery
## 1. Scan Network Range
`nmap 10.10.1.0/24 -sn -oA target | grep for | cut -d " " -f5`

| **Scanning Options** | **Description**                                                  |
| -------------------- | ---------------------------------------------------------------- |
| `10.10.1.0/24`       | Target network range.                                            |
| `-sn`                | Disables port scanning.                                          |
| `-oA target`         | Stores the results in all formats starting with the name 'target'. |
  
## 2. Scan IP List
`nmap -sn -oA target -iL hosts.txt | grep for | cut -d " " -f5`

|**Scanning Options**|**Description**|
|---|---|
|`-sn`|Disables port scanning.|
|`-oA target`|Stores the results in all formats starting with the name 'target'.|
|`-iL`|Performs defined scans against targets in the provided 'hosts.txt' list.|

## 3. Scan Multiple IPs
`nmap -sn -oA target 10.129.2.18 10.129.2.19 10.129.2.20| grep for | cut -d" " -f5`
