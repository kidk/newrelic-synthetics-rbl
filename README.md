# New Relic Synthetics RBL Checks

Use this script to test a set of IP address against a list of [DNSBLs](https://en.wikipedia.org/wiki/Domain_Name_System-based_Blackhole_List) providers. The script will fail when a match is found, which means on of the IP address is on a mail abuse list. The script is used in a combination with [New Relic Synthetics](https://www.newrelic.com/products/synthetics), so a paid New Relic license is required.

## License & Support

This project is distributed under the Apache 2 license and is provided AS-IS WITHOUT WARRANTY OR SUPPORT, although you can report issues and contribute to the project here on GitHub.

Please do not report issues with this software to New Relic Global Technical Support.

## Installation

1. Go to New Relic Synthetics and create a new API Test
2. Advised is to choose 1 location and set the schedule for once per day
3. Copy the script from [rbl-check.js](./rbl-check.js) and replace `listOfAddresses` with your own list

Example

```
var listOfAddresses = [
    "127.0.0.2",
    "127.0.0.3",
];
```

4. Add the adapted script to the New Relic Synthetics API Test and validate



## List of providers

### OpenRBL Blacklist
* DNS: openrbl.org
* Website: http://www.openrbl.org/


### Mail-abuse.org
* DNS: blackholes.mail-abuse.org
* Website: http://www.mail-abuse.org/


### Distributed Sender
* DNS: list.dsbl.org
* Website: http://dsbl.org/"


### SpamCop
* DNS: bl.spamcop.net
* Website: http://spamcop.net


### Sorbs Aggregate Zone
* DNS: dnsbl.sorbs.net
* Website: http://dnsbl.sorbs.net/


### Sorbs spam.dnsbl Zone
* DNS: spam.dnsbl.sorbs.net
* Website: http://sorbs.net


### Composite Blocking List
* DNS: cbl.abuseat.org
* Website: http://www.abuseat.org


### SpamHaus Zen
* DNS: zen.spamhaus.org
* Website: http://spamhaus.org


### Multi SURBL
* DNS: multi.surbl.org
* Website: http://www.surbl.org


### Spam Cannibal
* DNS: bl.spamcannibal.org
* Website: http://www.spamcannibal.org/cannibal.cgi


### dnsbl.abuse.ch
* DNS: spam.abuse.ch
* Website: http://dnsbl.abuse.ch/


### The Unsubscribe Blacklist(UBL)
* DNS: ubl.unsubscore.com
* Website: http://www.lashback.com/blacklist/


### UCEPROTECT Network
* DNS: dnsbl-1.uceprotect.net
* Website: http://www.uceprotect.net/en
