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

  proxy_ipcidr:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/proxy_ipcidr.yaml"
    interval: 86400
    path: ./rules/proxy_ipcidr.yaml

  proxy:
    behavior: "classical"
    type: http
    url: "https://raw.githubusercontent.com/pro1tocol/Global-Rules-Clash/refs/heads/rules/proxy.yaml"
    interval: 86400
    path: ./rules/proxy.yaml

# make the rules effctive
rules:
  - DOMAIN-SUFFIX,local,DIRECT,代理
  - DOMAIN-SUFFIX,jsdelivr.net,代理
  - DOMAIN-SUFFIX,gstatic.com,代理
  - DOMAIN-SUFFIX,docker.com,代理
  - DOMAIN-SUFFIX,github.io,代理
  - DOMAIN-SUFFIX,github.com,代理
  - DOMAIN-SUFFIX,githubassets.com,代理
  - DOMAIN-SUFFIX,githubusercontent.com,代理
  - RULE-SET,black,REJECT,no-resolve
  - RULE-SET,direct_ipcidr,DIRECT,no-resolve
  - RULE-SET,direct,DIRECT
  - RULE-SET,proxy_ipcidr,代理,no-resolve
  - RULE-SET,proxy,代理
  - MATCH,规则外路由选择
```