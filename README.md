# sectools

## List of tools

### OSINT
[ProjectDiscovery](https://github.com/projectdiscovery) - awesome tools for quick osint
- [subfinder](#subfinder)
- [httpx](#httpx)
- [naabu](#naabu)
- [dnsx](#dnsx)
- [nuclei](#nuclei)

*Domains*
- [dig](#dig)


## Install and use

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

## dnsx
[dnsx](https://github.com/projectdiscovery/dnsx) - is a fast and multi-purpose DNS toolkit allow to run multiple probes
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/dnsx/cmd/dnsx

# usefull commands
subfinder -silent -d hackerone.com | dnsx 
subfinder -silent -d hackerone.com | dnsx -silent -cname -resp
dnsx -l airbnb-subs.txt -wd airbnb.com -o output.txt
```

## nuclei
[nuclei](https://github.com/projectdiscovery/nuclei) - Nuclei is used to send requests across targets based on a template leading to zero false positives and providing fast scanning on large number of hosts.
```bash
# install
GO111MODULE=on go get -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei
nuclei -update-templates

# usefull commands
nuclei -u https://example.com
nuclei -list urls.txt
```

## dig
```bash
# get all dns records for the domain
dig any domain.com

# get specific type (A, NS, MX, TXT, SOA, etc..)
dig -t TXT domain.com
```
