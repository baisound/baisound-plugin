# baisound-plugin

<<サーバーフォルダ>>\plugins\baisound フォルダの下にconfig.yml を配置

内容を以下のようにする

```
tiktok:
  log_directory: "C:\\WorkFolders\\logs"  # ログを保存するディレクトリ（デフォルト: logs/tiktok）
  streamer: "<<TikTok ID>>"
  defaultmobname: "弱ったバイさん"
```

・log_directory・・・Windowsのどこにログを保存するのか
・streamer: "<<TikTok ID>>"・・・接続するTikTok IDを指定する
・defaultmobname・・・ギフターの名前で差し替えれないシチュエーションのデフォルトモブ名を指定する
