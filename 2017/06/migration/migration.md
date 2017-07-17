## 概要
多:多の関係をもつモデルの実装

## データ作成

ユーザーモデルを作成
(省略)

お気に入りリストを作成

```
bundle exec rails generate model FavoriteList name favoriter_type favoriter_id:integer deleted_at:datetime
bundle exec rake db:migrate
```

中間テーブルを作成

```
bundle exec rails generate model FavoriteListFavorite note favorite_list_id:integer favorite_id:integer deleted_at:datetime
bundle exec rake db:migrate
```

(参考)既存のお気に入りリストにカラムを追加

```
add_column :favorites, :favorite_list_id:integer
```

戻す場合

```
bundle exec rake db:version
ls -lrt db/migrate

rake db:rollback
rake db:version
```

rollbackのステップ数を指定するとき
```
rake db:rollback STEP=2
```


- migration マイグレーションファイル単体を作成する
- model モデルと一緒にマイグレーションファイルを作成する


## モデルに関連を追加

## ルーティングの変更


## controllerの作成


## jsonフォーマットの作成(representorっていうのかな？)

favorite_lists_controller.rb
rpresenter = FavoriteListFavorite


item.id = favorite.id
item.note = favarite_list.favorite.note

## 参考
http://qiita.com/zaru/items/cde2c46b6126867a1a64


reserved_optinon_food
-> reservation, option_food

owner_user
