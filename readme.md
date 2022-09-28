
Nginx configuration to host multiple servics on the same external ip. 

Ideal configuration for hosting multiple Openshift Clusters in a homelab environment, where you have only one internet facing ip available.

Also caters for internal internal DNS, so that the request is proxied to the internal private IP, not the global dns entry

Repeat the server section for each Openshift cluster you want to expose.

Forward external resolved host name to internal reolved host name.

nginx -c nginx.conf
