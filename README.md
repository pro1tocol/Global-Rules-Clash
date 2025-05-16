##### This repository is designed to streamline Clash(Premium) rules

##### Source: [https://github.com/pro1tocol/Global-Rules-Clash.git](https://github.com/pro1tocol/Global-Rules-Clash.git)

# Global-Rules-Clash

- ### HOW TO USED
| NODE | INSTRUCTIONS |
| :--- | :--- |
| DIRECT | Local switch |
| Modem | Load balancing |
| Social | Support social application |
| Work | Support work application |
#### DOWNLOAD
``` bash
git clone -b rules --single-branch https://github.com/pro1tocol/Global-Rules-Clash.git
mv Global-Rules-Clash rules
```
#### UPDATE
``` bash
git fetch origin rules
git pull origin rules
```
- ### LIST
| NAME | TYPE | FUNCTION | DNS |
| :---: | :---: | :---: | :---: |
| blacklist.yaml | global | disable connect| NO |
| direct.yaml | direct | local connect | YES |
| direct_ipcidr.yaml | direct | local connect | NO |
| modem.yaml | proxy | proxy connect | YES |
| social.yaml | proxy | proxy connect | YES |
| work.yaml | proxy | proxy connect | YES |
| proxy_ipcidr.yaml | proxy | proxy connect | NO |

