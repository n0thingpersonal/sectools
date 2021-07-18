# sectools

## OSINT


[ProjectDiscovery](https://github.com/projectdiscovery) - awesome tools for quick osint
- subfinder
- httpx


[subfinder](https://github.com/projectdiscovery/subfinder) - passive subdomain discovery tool that discovers valid subdomains
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder

# Usefull commands
subfinder -d example.com
subfinder -d example.com -o output.txt
``

[httpx](https://github.com/projectdiscovery/httpx) - is a fast and multi-purpose HTTP toolkit allow to run multiple probers
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/httpx/cmd/httpx

# usefull commands
httpx -l hosts.txt -silent
subfinder -d hackerone.com | httpx -title -tech-detect -status-code -follow-redirects
```
