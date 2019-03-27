# probhat.im
:globe_with_meridians: Online Probhat Keyboard

## TODO

- [x] Support mobile browser
- [x] Remove bootstrap.css
- [ ] Add FAQ pages
- [ ] Multiple notepad
- [ ] Save text to local storage
- [ ] Warn user when hitting Ctrl+W

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
