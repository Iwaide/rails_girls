## WHAT
RailsGirls用の雛形です

## WHY
- Rails Tutorialより軽そう
- Rails Girlsはコーチの存在を前提としているので教える側にもガイドがある

## HOW
### Docker for Windowsをインストール
[Windows10 に Docker for Windows をインストールする手順](https://qiita.com/busonx/items/849a861d8bb93c71bbe7)

- Windows10ProじゃないとHyper-vが使えないので注意

### railsアプリを作る
``docker-compose run --rm app rails new . --force --database=mysql --skip-bundle``

### puma.rbとdatabase.ymlの設定をする
[Docker + Rails + Puma + Nginx + MySQL](https://qiita.com/eighty8/items/0288ab9c127ddb683315)

### dockerイメージを作成する
``docker-compose build``

### dockerコンテナを立ち上げる
``docker-compose up``

### DBを作成する
``docker-compose run --rm app rails db:create``

TODO: DBの永続化についてもっと調べる
- MySQLのデータが
- volumesは本当にdocker-compose downで消えてしまうのか