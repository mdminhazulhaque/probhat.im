# probhat.im
:globe_with_meridians: Online Probhat Keyboard

## TODO

* Support mobile browser
* Add FAQ pages
* Remove bootstrap.css

## nginx

```
server {
        listen 80;
        server_name probhat.im www.probhat.im;

        root /www/probhat;
        index index.html;

        location / {
            try_files $uri $uri/ /index.html;                
        }
        
        location /app.cache {
            add_header Content-Type "text/cache-manifest";
        }
        
        location ~ /\.git {
            deny all;
        }
}
```
