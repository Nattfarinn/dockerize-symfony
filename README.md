# dockerize-symfony
Dockerize Symfony development stack (PHP, Yarn, Nginx, DB)

# Install & Update

```
$ wget https://raw.githubusercontent.com/Nattfarinn/dockerize-symfony/master/dockerize -O /usr/local/bin/dockerize && chmod +x /usr/local/bin/dockerize
```

# Usage

```
usage: dockerize [-h] [--php-version [VER]] [--db-engine [ENGINE]]
                 [--db-version [VER]] [--network [NETWORK]] [--tld [TLD]]
                 [--ssh-path [SSH]] [-x] [-f]
                 source [target]

Prepare Docker stack environment for Symfony application

positional arguments:
  source                repository to be cloned
  target                target directory and path (default:
                        ./{repository_name}.docker)

optional arguments:
  -h, --help            show this help message and exit
  --php-version [VER]   PHP version (default: 7.3)
  --db-engine [ENGINE]  Database engine (default: postgres)
  --db-version [VER]    Database version (default: latest)
  --network [NETWORK]   Docker external network to be shared with
                        jwilder/nginx-proxy (default: proxy)
  --tld [TLD]           Top-level domain to be used for vhost creation
                        (default: test, example: repository_name.dev.test)
  --ssh-path [SSH]      Local SSH directory to be mounted with application
                        containers (default: ~/.ssh)
  -x, --xdebug          Setup additional XDebug docker service
  -f, --force           Overwrite target content if exists (involves rm -Rf on
                        target path, use with caution!)
```

# Disclaimer
Feel free to use it but keep in mind I did it for my own, personal convenience. Don't expect it to be suitable for your use case.
