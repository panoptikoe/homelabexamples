This is a very old concept but I found it to be pretty useful, because I added the cronjobs. It requires every Linux host in your network to have this in `/etc/apt/conf.d/02proxy`:
````Bash
Acquire::https::Proxy "https://cache.local.yourdomain.com:443";
#Acquire::http::Proxy "http://directipaddressoftheabove:3142";
Acquire::https::Proxy::download.docker.com "DIRECT";
Acquire::https::Proxy::ppa.launchpadcontent.net "DIRECT";
Acquire::https::Proxy::raw.githubusercontent.com "DIRECT";
````
Sometimes, the second line can be needed so I included it. You can uncomment it if you need it to be there, or remove the other lines. I found them to be useful.
