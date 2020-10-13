# postgres-pro-std-python
 Postgres Pro Standard 12 + PL/Python 3 enable as SQL developer


Data path for volume `/var/lib/pspro`

Preinstalled python libs
```
pyxdameraulevenshtein
pystemmer
```


```
version: '3.1'
services:
  sql:
    image: gpanteleev/postgres-pro-std-python:latest
    restart: always
    ports:
      - 5432:5432
    volumes:
      - /somedir/pspro:/var/lib/pspro
    environment:
      POSTGRES_PASSWORD: somepass
      POSTGRES_USER: postgres
      shared_buffers: 12GB
      effective_cache_size: 42GB
      max_wal_size: 4GB
      min_wal_size: 2GB
      work_mem: 12MB
      maintenance_work_mem: 2GB
      wal_buffers: 16MB
      checkpoint_completion_target: 0.9
      default_statistics_target: 100
```

