# Check Reputation
![Generic badge](https://img.shields.io/badge/python-3.7-blue.svg) [![Twitter](https://img.shields.io/badge/Twitter-@pulsecode-blue.svg)](https://twitter.com/pulsecode)

`check_rep.py` Check IP or Domain reputation against 400+ open-source Blacklists.  Utilizes asynchronous execution with [threads](https://docs.python.org/3/library/concurrent.futures.html) for faster querying.


Option to create a Geolocation map file using coordinates derived from [freegeoip.live](https://freegeoip.live), or MaxMind [GeoLite](https://dev.maxmind.com).

**Note:** 
Use of VirusTotal option requires an API key.  The service is free, however you must register for an account to aquire an API key.

```
usage: check_rep.py [-h] [-q query] [--log] [--vt]
                    [--fr | --mm | --mx FILE [FILE ...]]

Check IP or Domain Reputation

required arguments:
  -q query              query ip address or domain

optional arguments:
  -h, --help            show this help message and exit
  --log                 log results to file
  --vt                  check virustotal
  --fr                  use freegeoip for geolocation
  --mm                  use maxmind (geolite) for geolocation
  --mx FILE [FILE ...]  geolocate multiple ip addresses or domains

    Geolocation Options
    --------------------
    freegeoip [freegeoip.live]  - free/opensource geolocation service                  
    maxmind   [dev.maxmind.com] - uses a geolite db file for geolocation         
    
    * NOTE: 
     Use of VirusTotal option requires an API key.  
     The service is free, however you must register 
     for an account to aquire an API key.
``` 
# Installation

```
git clone https://github.com/dfirsec/check_rep.git
cd check_rep
pip install -r requirements.txt
```

## Example Run
[![asciicast](https://asciinema.org/a/r6VDD8QaHsaj3Fzo1wjU96BmQ.svg)](https://asciinema.org/a/r6VDD8QaHsaj3Fzo1wjU96BmQ)

## Geolocation Map File
![alt text](images/geo_ip_map_example.png)
