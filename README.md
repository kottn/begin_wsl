# begin_wsl
:beginner: はじめてのWSL

## WSL ?
* **W**indows **S**ubsystem for **L**inux （Windows で Linux が使える Microsoft 公式ソフト）
* **Microsoft社のサポート権がつきます（重要）**
>:link: [What's new in WSL in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/10/11/whats-new-in-wsl-in-windows-10-fall-creators-update/)
>This means that if you run into unexpected issues or problems with WSL, you can contact Microsoft Support to file a support ticket that will be managed through the normal channels.
* なんか設定しててよくわからなくなったら消してやり直せばいい
* 市民権を得ている Ubuntu が使える

## やること
Windows10 で **Ubuntu 16.04** を動かす

## インストール
[シス管系女子 - 漫画でわかるWSL](http://system-admin-girl.com/comic/begins/sp-wsl/)
注） 非常にわかりやすいが、読むのに勇気がいる。

### 要約
1. Windows Update を**最新**に
1. 

## 初期設定
### リポジトリの参照先を日本に
* デフォルトが`http://archive.ubuntu.com/ubuntu/`なので遅い。日本国内のミラーに変更する。

<script src="https://gist.github.com/kottn/6b08a7c20f917cedb1d68f57fd8dafb5.js"></script>

* `source.list`を編集
```
$ sudo vi /etc/apt/source.list
```
* `deb http://security.ubuntu.com/ubuntu/ なんとかかんとか～`の行**以外を**コメントアウト



### とりあえず
```
$ sudo apt update
$ sudo apt upgrade
```
### X11を有効化
```
$ sudo apt install x11-apps
$ echo "export DISPLAY=localhost:0.0" >> ~/.bash_profile
$ source ~/.bash_profile
$ xeyes   # 確認
```

### apt
```
$ sudo apt install \
firefox
```
