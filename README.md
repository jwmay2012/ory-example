Ports `443, 50000` must be free

`docker compose up`

https://ui.ory.localhost  
https://traefik.ory.localhost  
https://prometheus.ory.localhost  
https://whoami.ory.localhost  
https://grafana.ory.localhost  

https://spicedb-dashboard.ory.localhost  
https://spicedb-http.ory.localhost


Ignore and Proceed with invalid certificates


grpc://spicedb-grpc.ory.localhost:50000

You may have to add these urls to your `/etc/hosts` file to allow 
applications other than Chromium to route properly. 
```
127.0.0.1	keto-read.ory.localhost keto-write.ory.localhost spicedb-dashboard.ory.localhost spicedb-grpc.ory.localhost spicedb-http.ory.localhost
```

We should be able to hide the GRPC service behind an HTTPS endpoint with Traefik h2c
https://doc.traefik.io/traefik/user-guides/grpc/  
Haven't fussed with the certs yet and the Host or HostSNI rules wouldn't recognize
the hostname for routing. Maybe a grpc client issue?