# powershell-empire-docker
Dockerized Powershell Empire

Get up and running with [Powershell Empire](http://www.powershellempire.com/).

Use the following command to expose the ports commonly used by Powershell Empire and create two bound volumes. /Empire/data is where loot will be stored, and /Empire/tmp is bound to the /tmp directory of the container (where stager output is placed by default):

```
docker run -it -p 80:80 \
-p 443:443 -p 8080:8080 \
-p 8081:8081 \
-v ~/Empire/tmp:/tmp 
-v ~/Empire/data:/opt/Empire/data/downloads \
hoptimumthreat/powershell-empire
```
