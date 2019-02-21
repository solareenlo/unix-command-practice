# unix-command-practice

## mkdirを使って一気にファイルを複数作成する
```bash
# app1, app2, ... app39, app40というフォルダを一斉に作成する方法
mkdir app{1..40}
```

## 一般ユーザーと管理ユーザー
```bash
# 一般ユーザーだと
[solareenlo@localhost ~]$

# 管理ユーザーだと
[solareenlo@localhost ~]#
```

## UNIXシステムのディレクトリの大体の構成
- binには, バイナリデータが入ってる.
- binには, catやcpといった, システムを動かすための基本コマンドの実行ファイルがある.
- etcには, アプリケーションの設定ファイルが入っている.
- homeには, 各ユーザーのホームディレクトリが入ってる.
- sbinには, システム管理用のコマンドが入っている.
- usrには, 一般的なアプリケーションが格納されてる.
- varには, システムのログファイルなどの頻繁に書き換わるようなファイルが入ってる.

## ディレクリを移動する
```bash
# 現在いるディレクトリを表示
pwd

# 画面をきれいにするには
clear
# Control + l

# ディレクトリへ移動
cd path/to/directory/

# 1つ上の階層へ戻る
cd ..

# 直前のディレクトリへ戻る
cd -

# ホームディレクトリへ戻る
cd
```

## ディレクトリを操作する
```bash
# ディレクトリを新規作成
mkdir test

# ディレクトリ一覧表示
ls

# ディレクトリをコピー
cp -r test test2

# test3ディレクトリの中にconfigディレクトリを一気に作成する
makir -p test3/config

# test3ディレクトリをtest2ディレクトリに移動する
mv test3 test2

# 空のディレクトリを削除する
rmdir test2/test3/config

# 空でないディレクトリを削除する
rm -r test2
```

## ファイル操作
```bash
# file.txtの中身を全部一斉に見る
cat path/to/file.txt

# file.txtの中身を少しずつ見るには
less path/to/file.txt
# 矢印キーでスクロール
# space で下へ移動
# Control + F で一画面先へ移動
# Control + B で一画面前へ移動
# g でファイル先頭へ移動
# G でファイル末尾へ移動
# q で終了

# 現在のディレクトリにファイルコピー
cp path/to/file.txt .

# 現在のディレクトリにあるファイルを名前変更
mv file.txt file2.txt

# ファイルを削除
rm file2.txt
```

## bashの便利機能
```bash
# 操作をとりあえずキャンセル
# CTRL + C

# コマンドの履歴検索
# CTRL + R
# そこで何かしら前に使ったコマンドを途中まで入力してtabキーを押して補完して, エンターキーを押すと実行される
```
