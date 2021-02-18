# afraid-dns-updater
IP update script for https://freedns.afraid.org/

Similar to DuckDNS, any many others, Afraid.org offers free DNS services and this script will keep your IPs updated rather than using a docker to keep it updated.

The usage is very easy, but you will need to set the update URLs for your domains.

Log into your Afraid DNS account and then go to the version 2 dynamic update interface page (https://freedns.afraid.org/dynamic/v2/)

For each of the subdomains you want to update just paste the update URL into the script.

curl http://sync.afraid.org/u/TOKEN/
  
Note the trailing slash at the end of the url.  It is required.

Your script will look like this:

#!/bin/bash
curl http://sync.afraid.org/u/YOUR_TOKEN/
