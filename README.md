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

★各種シーケンス図

https://www.mermaidchart.com/raw/35eebe05-8007-4f82-993e-31a6d91fa728?theme=light&version=v0.1&format=svg

★各種REST APIドキュメント

http://52.195.57.50/api/xpeC4I0Z1Xu2vOrUg7KE0kxut9Bwxx#/ライセンス/d7fc17545a832a063e504e32431a6f0f

# バージョン履歴
## 4.0.6
ルーレット機能同梱
plugins/roulette/ルーレット毎のファイルサンプルがおいてあります

## 4.0.5
コマンド実行時の候補補完機能がリファクタリングのタイミングで実装から外れたのを再度実装

## 4.0.4
コマンド実行時に@pを置き換え対象にしてしまっていた事により発生していた不具合修正

## 4.0.3
実装機能：
コマンドブロックやTikFinity等プレイヤー自身によるコマンド以外の実行時に、{PlayerMe}を指定しておくとオンラインプレイヤー名で置き換え実行してくれる機能実装

4.0.2から発生している問題
・使えるファイルコマンドの補完機能

## 4.0.2
ライセンスバリデーションが実装されました
今後の実装に柔軟性を持たせる為の大幅なリファクタリングを実施しました

## 3.0.2
ライセンスキーに対応しています
baisound.admin.properties を開いて運営に発行してもらったライセンスキーとトークンを設定してください

## 2.0.0
ギフト情報の記録機能追加
config.yml に以下ログを保存するディレクトリ先を追記すること

```
  log_directory: "C:\\WorkFolders\\logs"  # ログを保存するディレクトリ（デフォルト: logs/tiktok）
```

## 2.0.1
対応するギフトID、ギフトコスト、ギフト名、ギフト画像URLの一覧作成機能追加
config.yml に以下情報保存先ディレクトリを追記すること

```
  gift_directory: "C:\\WorkFolders\\logs\\giftimages"
```

## 2.0.2
TikTokへ接続出来ない状態の場合にエラーが出ていたのをofflineとログに記載されるように修正
