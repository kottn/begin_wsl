# 便利な設定
## Windows側 のよく使う場所をホームにリンク
* Windows 側のファイルを Linux から見れたら便利。
* Linux 側から見ると C ドライブは`/mnt/c`、E ドライブは`/mnt/e`にある。
* たとえばWindowsでいう`C:\Users\tarou\Desktop`は、Linuxからだと`/mnt/c/Users/tarou/Desktop`である。
* これを踏まえて下記を（`<path>/<to>`のところのパスを自分の設定に置き換えて）実行する。
```
$ cd      # どこにいてもホームにもどれるコマンド
$ ls	  # まだ何も見えないはず
$ ln -s /mnt/<path>/<to>/Desktop .
$ ln -s /mnt/<path>/<to>/Downloads .
$ ln -s /mnt/<path>/<to>/Documents .
$ ls      # 何かできたかな
$ ls -l   # リンク先確認
```

## 右クリック したらそこで Bash を開ける設定
1. [`bash_here.reg`](https://raw.githubusercontent.com/kottn/begin_wsl/master/bash_here.reg)をクリック、ダウンロード（名前を付けて保存）。
1. ダブルクリック。
1. はい、はい、OK
1. 好きなところで 右クリック ⇒ 「Bash をここで開く！」
1. なお、右クリック => b でも起動すると思います。

これで全ての設定が終わりです。

[はじめにもどる](./README.md)
