munin-nginx_response
====================

Munin plugin for nginx response breakdowns

Gives munin results for cache status, HTTP response code, unique ips

Requires that nginx access logs have $upstream_cache_status as the last column

Requires logsince to parse the logs

The parse_script should reference the munin plugin

User configurable stuff
```
[nginx_response]
  env.logsince_script /usr/local/sbin/logsince
  env.access_log /var/log/nginx/access.log
  env.parse_script /usr/share/munin/plugins/nginx_response
  env.domains www.vice.com m.vice.com
```
