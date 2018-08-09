# [Docker_for_Ruby](https://github.com/prgyukke/Docker_for_Ruby)
## はじめに
Ruby開発環境用のDockerです。  
プロジェクトディレクトリを`app`コンテナの`/home/ruby`にマウントしています。  
OSXにて、[Docker For Mac](https://www.docker.com/docker-mac)のインストール前提です。  
[Docker Community Edition for Mac - Docker Store](https://store.docker.com/editions/community/docker-ce-desktop-mac)の[Get Docker]をクリックしてダウンロード後、インストールしてください。  

### 各バージョン
- Ruby 2.5
- MySQL 5.7


## 環境構築
### 初回のみ
```
$ git clone git@github.com:prgyukke/Docker_for_Ruby.git
$ cd Docker_for_Ruby/
$ rm -rf .git
$ docker-compose up -d
```

### 2回目以降
```
$ docker-compose up -d
```

### コンテナに入る際
#### ruby用コンテナ
```
$ docker exec -it docker_for_ruby_app_1 /bin/bash
```

#### db用コンテナ
```
$ docker exec -it docker_for_ruby_db_1 /bin/bash
```

### コンテナを抜ける際
```
# コンテナ上にて
# exit
```

### 開発終了時
```
$ docker-compose down
$ docker rmi docker_for_ruby_app_1
```

## MySQL
- host
	- db
- user / password
	- root / yQqDx.4(Cnue
	- ruby / GdS)FP6*B7zJ
