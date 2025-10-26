<h1 align="center">
  <br>
  <a href="https://github.com/fieu/geoip"><img src="https://i.imgur.com/0IwBubm.png" width="200"></a>
  <br>
  geoip
  <br>
  <br>
</h1>

<h4 align="center">Retreive geographical IP information on the command-line.</h4>

## Proposal
I wanted an easy way to check IP address info without having to open a browser every time, and since I was in the terminal already, it would be perfect to have it in the terminal.

## Disclaimer
The code is poor, and I'm using ipinfo.io to grab the geographical IP address info. Unfourtunately, ipinfo.io only allows up to 1,000 requests per day. I'm working on either building my own solution or finding another database lookup service that has unlimited requests. I'm using this as one of my first Bash projects to get better at Bash and learn as much as I can while building up this piece of software.

## Requirements
* cURL
* SHML ([http://shml.xyz](http://shml.xyz))
* jsawk ([https://github.com/micha/jsawk](https://github.com/micha/jsawk))
* You need to have the `js` interpreter installed like [SpiderMonkey](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey).

## Install
* `sudo bash -c 'curl -L https://raw.githubusercontent.com/fieu/geoip/master/geoip -o /usr/local/bin/geoip && chmod +x /usr/local/bin/geoip'`

## Usage
```text
geoip [-h] [IP] -- Get GeoIP information on the command-line.

options:
    -h  show this help text
```
### Example
Get information for the address 52.2.59.254:
```text
[~]$ ./geoip 52.2.59.254
IP: 52.2.59.254
Hostname: ec2-52-2-59-254.compute-1.amazonaws.com
City: Ashburn
Region: Virginia
Country: US
Coordinates: 39.0481,-77.4728
Organization: AS14618 Amazon.com, Inc.
```
