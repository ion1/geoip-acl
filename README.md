# geoip-acl – Country whitelisting for servers using GeoIP

Depends on `geoiplookup`/`geoiplookup6` from [Maxmind][geoip-api-c]. See the
[geoip-bin][geoip-bin-debian] package on Debian and derivatives.

[geoip-api-c]:      https://github.com/maxmind/geoip-api-c
[geoip-bin-debian]: http://packages.debian.org/geoip-bin

Example of usage: whitelist Finland, Jamaica and Taiwan:

`/etc/hosts.deny`:

```
sshd : ALL : aclexec ! /opt/geoip-acl/geoip-acl FI,JM,TW %a
```

# geoip-update-free – Update the local copy of Maxmind GeoLite Free database

Depends on `curl`.

To be run from cron (using `>/dev/null 2>&1` or [chronic][moreutils])).

[moreutils]: http://joeyh.name/code/moreutils/
