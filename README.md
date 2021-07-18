# sectools

## OSINT


[ProjectDiscovery](https://github.com/projectdiscovery) - awesome tools for quick osint
- [subfinder](##subfinder)
- [httpx](##httpx)
- [naabu](##naabu)


## subfinder
[subfinder](https://github.com/projectdiscovery/subfinder) - passive subdomain discovery tool that discovers valid subdomains
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder

# Usefull commands
subfinder -d example.com
subfinder -d example.com -o output.txt
```

## httpx
[httpx](https://github.com/projectdiscovery/httpx) - is a fast and multi-purpose HTTP toolkit allow to run multiple probers
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/httpx/cmd/httpx

# usefull commands
httpx -l hosts.txt -silent
subfinder -d hackerone.com | httpx -title -tech-detect -status-code -follow-redirects
```

## naabu
[naabu](https://github.com/projectdiscovery/naabu)
```bash
# intall
GO111MODULE=on go get -v github.com/projectdiscovery/naabu/v2/cmd/naabu

# usefull commands
naabu -p 80,443,21-23 -host hackerone.com
```
