# baisound-plugin

<<サーバーフォルダ>>\plugins 直下にダウンロードしたJARファイルを設置する

設置したあとサーバーを起動する

※ サーバーの起動の仕方についてはここでは触れませんので別途お調べくださいませ。

<<サーバーフォルダ>>\plugins\baisound フォルダの下にconfig.yml を配置

内容を以下のようにする

```
tiktok:
  log_directory: "C:\\WorkFolders\\logs"  # ログを保存するディレクトリ（デフォルト: logs/tiktok）
  gift_directory: "C:\\WorkFolders\\logs\\giftimages"
  streamer: "<<TikTok ID>>"
  defaultmobname: "弱ったバイさん"
```

・log_directory・・・Windowsのどこにログを保存するのか

・streamer: "<<TikTok ID>>"・・・接続するTikTok IDを指定する
※ <<TikTok ID>> を自分のIDに置き換えてくださいませ。例：TikTok IDが@thisisid だったとする。thisisid を設定するので記述は「streamer: "thisisid"」となる

・defaultmobname・・・ギフターの名前で差し替えれないシチュエーションのデフォルトモブ名を指定する

# 実行コマンドファイルについて

<<サーバーフォルダ>>\plugins\baisound フォルダ配下にコマンドファイルを設置して頂く事で再起動されたマイクラサーバーでコマンドが使用できるようになります

https://github.com/baisound/baisound-command

# 実行コマンドファイルの使い方について

クライアントにて以下の要領で実行可能です

Tボタンを押してコマンド入力モードに切り替えてコマンドを入力

例
/baisound zombie 10 5 test
ゾンビを１０体５Tickの速度でゾンビにtestという名前をつけて沸かせる
/baisoundまで入力すると設置されている実行コマンドが実行可能一覧としてリスト表示されます。


# バージョン履歴

## 2.0.2
TikTokへ接続出来ない状態の場合にエラーが出ていたのをofflineとログに記載されるように修正

## 2.0.1
対応するギフトID、ギフトコスト、ギフト名、ギフト画像URLの一覧作成機能追加
config.yml に以下情報保存先ディレクトリを追記すること

```
  gift_directory: "C:\\WorkFolders\\logs\\giftimages"
```

## 2.0.0
ギフト情報の記録機能追加
config.yml に以下ログを保存するディレクトリ先を追記すること

```
  log_directory: "C:\\WorkFolders\\logs"  # ログを保存するディレクトリ（デフォルト: logs/tiktok）
```
