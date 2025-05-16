##### This repository is designed to streamline Clash(Premium) rules

##### Reference [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules)

# Global-Rules-Clash

> ### Check list
#### View Branches: [Rules](https://github.com/pro1tocol/Global-Rules-Clash/tree/rules)

> ### How to add rules in Clash
#### You need add it into 'config.yaml'
``` bash
# include the rules
rule-providers:
  black:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/black.yaml"
    interval: 86400
    path: ./rules/black.yaml

  direct_ipcidr:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/direct_ipcidr.yaml"
    interval: 86400
    path: ./rules/direct_ipcidr.yaml

  direct:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/direct.yaml"
    interval: 86400
    path: ./rules/direct.yaml

  work:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/work.yaml"
    interval: 86400
    path: ./rules/work.yaml

  social:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/social.yaml"
    interval: 86400
    path: ./rules/social.yaml

  modem:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/modem.yaml"
    interval: 86400
    path: ./rules/modem.yaml

rules:
  - DOMAIN-SUFFIX,local,DIRECT
  - DOMAIN-SUFFIX,cloudflare.com,DIRECT
  - DOMAIN-SUFFIX,jsdelivr.net,Social
  - DOMAIN-SUFFIX,gstatic.com,Social
  - DOMAIN-SUFFIX,docker.com,Work
  - DOMAIN-SUFFIX,github.io,Work
  - DOMAIN-SUFFIX,github.com,Work
  - DOMAIN-SUFFIX,githubassets.com,Work
  - DOMAIN-SUFFIX,githubusercontent.com,Work
  - RULE-SET,black,REJECT,no-resolve
  - RULE-SET,direct_ipcidr,DIRECT,no-resolve
  - RULE-SET,direct,DIRECT
  - RULE-SET,modem,Modem
  - RULE-SET,work,Work
  - RULE-SET,social,Social
  - MATCH,Match
```