# geoip-acl – Country whitelisting for servers using GeoIP

Example of usage: whitelist Finland, Jamaica and Taiwan:

`/etc/hosts.deny`:

```
sshd : ALL : aclexec ! /opt/geoip-acl/geoip-acl FI,JM,TW %a
```

# geoip-update-free – Update the local copy of Maxmind GeoLite Free database

To be run from cron (using `>/dev/null 2>&1` or
[chronic](http://joeyh.name/code/moreutils/)).
