# dokku-proxy-to-minio
Dokku App for proxy to minio

## Usage

On dokku host:

```
$ dokku apps:create proxy-to-minio
-----> Creating proxy-to-minio...
$ dokku config:set proxy-to-minio MINIO_SERVERS="minio1.example.com:9000 minio2.example.com:9000 minio3.example.com:9000"
-----> Setting config vars
       MINIO_SERVERS:  minio1.example.com:9000 minio2.example.com:9000 minio3.example.com:9000
-----> Restarting app proxy-to-minio
 !     App proxy-to-minio has not been deployed
```

On some host:

```
$ git clone https://github.com/znz/dokku-proxy-to-minio
$ git remote add dokku dokku@dokku.me:proxy-to-minio
$ git push dokku master
```

## see also

- <https://docs.min.io/docs/setup-nginx-proxy-with-minio.html>
- <https://github.com/dokku/dokku/blob/aa63e79aecafe226ce826497b12c5e74148d0e8a/plugins/nginx-vhosts/templates/nginx.conf.sigil>
