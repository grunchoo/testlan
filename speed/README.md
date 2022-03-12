# HTML5 Speedtest

Speedtest para la LAN


## Nginx config example:
```
  server {
    listen 80;
    server_name speed.nubenautas.net;
    location = /favicon.ico {
      alias /home/mencargo/src/nubenautas/public/favicon.ico;
    }
    location / {
      root /home/mencargo/src/speed;
    }
    location /ip {
      default_type text/plain;
      return 200 "${remote_addr}";
    }
    location /empty {
      default_type text/plain;
      return 200;
    }
  }
```


