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
1. タスクバーの検索機能（Windowsキー）

## 初期設定
#### リポジトリ参照先の変更
* 国内ミラーの有効化
* `/etc/apt/sources.list.d/`の下に`jaist.list`と`yamagata.list`を置く。
```
$ cd /etc/apt/sources.list.d \
    && sudo curl -LO https://raw.githubusercontent.com/kottn/begin_wsl/master/jaist.list \
    && sudo curl -LO https://raw.githubusercontent.com/kottn/begin_wsl/master/yamagata.list
```
* デフォルト設定`archive.ubuntu.com`の無効化
```
$ sudo vi /etc/apt/source.list
```
* `deb http://archive.ubuntu.com/ubuntu/ ほにゃらら...`の行をコメントアウト。
* `deb http://security.ubuntu.com/ubuntu/ ほにゃらら...`の行はそのまま。
* アップデートしておく
```
$ sudo apt update
$ sudo apt upgrade
```

### X11の有効化
```
$ sudo apt install x11-apps
$ echo "export DISPLAY=localhost:0.0" >> ~/.bash_profile
$ source ~/.bash_profile
$ xeyes
```

### 基本パッケージ
```
$ sudo apt install \
firefox
```
