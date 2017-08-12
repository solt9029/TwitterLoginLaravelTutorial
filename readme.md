# 目的

LaravelからSocialiteを利用してTwitterのログインを実装することです

# 環境構築

## 使用したバージョン一覧

- docker-compose: 1.11.1

- docker: 1.13.1

- php: 5.6.28

- laravel: 5.4.23

## 手順

```
cd TwitterLoginLaravelTutorial
composer install
cp .env.example .env
```

.envを編集します  
自分のTWITTER_CLIENT_ID・TWITTER_CLIENT_SECRET・CALLBACK_URLを入力してください  
docker-compose.ymlなどを変更する場合にはDBの設定なども見直してください

```
cd docker.twitterloginlaraveltutorial
docker-compose up -d
docker exec -it dockertwitterloginlaraveltutorial_web_1
cd /var/www/html
php artisan migrate
```

これで準備完了です  
[http://docker.app:8005](url)にアクセスするとTwitter利用ログイン画面が出てくると思います