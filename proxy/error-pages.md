# custom error pages

```bash
git clone https://github.com/HttpErrorPages/HttpErrorPages.git data/nginx/error_pages
mkdir -p data/nginx/custom
```
You can add a file server_proxy.conf in your /data/nginx/custom with your content example to set the custom error page globaly :

```ini
error_page 400 /error_pages/HTTP400.html;
error_page 401 /error_pages/HTTP402.html;
error_page 402 /error_pages/HTTP402.html;
error_page 403 /error_pages/HTTP403.html;
error_page 404 /error_pages/HTTP404.html;
error_page 500 /error_pages/HTTP500.html;
error_page 501 /error_pages/HTTP501.html;
error_page 502 /error_pages/HTTP502.html;
error_page 503 /error_pages/HTTP503.html;
proxy_intercept_errors on;

location /error_pages/ {
            alias /data/nginx/error_pages/dist/;
                internal;
}
```
