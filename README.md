# template for prometheus+grafana+nginx in docker-compose

- prometheus_data folder needs to be accesible to user `nobody`, so run `chown -R nobody:nogroup prometheus_data/` before you compose up.  

- when adding the grafana prometheus data source, dont forget to reference to `prometheus:9090` for url instead of localhost.  

- if you are using node_exporter then use your private ip for `prometheus.yml` (since localhost is the prometheus container itself).  

- also use the private ip, when proxy_passing on nginx.conf.  

- lastly, dont forget to create a `htpasswd` file for prometheus since its open to the public by default.  
