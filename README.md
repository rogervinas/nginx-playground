# NGINX playground 

## Run

```
docker compose up -d
curl -w'\n' http://localhost:8080/hello
curl -w'\n' http://localhost:8080/hello -H 'X-Forwarded-For: 0.0.0.1'
curl -w'\n' http://localhost:8080/hello -H 'X-Forwarded-For: 0.0.0.1, 0.0.0.2'
curl -w'\n' http://localhost:8080/hello -H 'X-Forwarded-For: 0.0.0.1, 0.0.0.2, 0.0.0.3'
curl -w'\n' http://localhost:8080/hello -H 'X-Forwarded-For: 0.0.0.1, 0.0.0.2, 0.0.0.3, 0.0.0.4'
```

## Documentation

* http://nginx.org/en/docs/http/ngx_http_map_module.html
* http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_set_header
* http://nginx.org/en/docs/varindex.html
