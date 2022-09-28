
# Nginx configuration to host multiple SSL services on the same external ip, based on host name. 

**Ideal configuration for hosting multiple Openshift Clusters in a homelab environment, where you have only one internet facing ip available.**

Also caters for internal DNS, so that the request is proxied to the internal private IP, not the global dns entry

Repeat the server section for each Openshift cluster you want to expose.

xxx.apps.cn.domain.com (External DNS) -> nginx -> xxx.apps.cn.domain.com (internal DNS)

Forward external resolved host name to internal reolved host name.

nginx -c nginx.conf
