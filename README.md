# rails-react-postgres-boilerplate
rails, react, postgresでプロジェクトを開始するときのテンプレートリポジトリです。
上記の技術スタックでプロジェクトを始める際はこちらのリポジトリをforkして始めます。

## 設定
### cloneした直後の手順
```
docker compose run api bundle exec rake db:create
docker compose build
docker compose up
```