# docker-nginx-unzip
[Alpine-based nginx](https://github.com/nginxinc/docker-nginx) compiled with  [unzip module](https://github.com/youzee/nginx-unzip-module)

# Usage:
```bash
docker run --rm --name nginx -p 80:80 -v /path/to/nginx.conf:/etc/nginx/nginx.conf:ro -v /root/with/zips:/var/www malinskiy/docker-nginx-unzip
```

# Notes
I removed the *text/plain* header from the source of the *nginx-unzip-module* to allow setting this in the nginx.conf 
Otherwise your browser will treat css+js as *text/plain*.

Don't forget to push the proper config to nginx, take a look inside ```sample``` folder
