# Docker x Rails(Mysql)実行環境
  

``` bash
#Ruby
2.5.3
#Rails
5.2.2

```
## Usage
```
$ cd backend
$ docker-compose run web rails new . --force --database=mysql --skip-bundle
$ vi config/database.yml(defaultのpasswordをpassword、defaultのhostをlocalhostからdbに編集)
$ docker-compose build && docker-compose up -d
$ docker-compose run web rails db:create
$ docker exec -it web /bin/sh
