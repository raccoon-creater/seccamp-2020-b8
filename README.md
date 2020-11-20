# seccamp-2020-b8

課題１

・ユーザの新規作成
insert into users values(2,'kadai1','kadai1',2020-11-15 10:27:59.284594,2020-11-15 10:27:59.284594);

・既存ユーザのname/email
update users set name = 'kadai1-2',email = 'kadai1-2' where name = 'kadai1';

・既存ユーザの削除
delete from users where id = 2;

課題2

redisを利用するためconfigファイルの修正（./config/environments/development.rb）

  config.cache_store = :null_storeを下記に変更
  config.cache_store = :redis_store, "redis://localhost:6379/0/cache"

