# begin_wsl
:beginner: はじめてのWSL

## WSL ?
* **W**indows **S**ubsystem for **L**inux
* WindowsでLinuxが使えるMicrosoft公式アプリ
* つまりサポート権がつきます（重要）
* なんか設定しててよくわからなくなったら消してやり直せばいい
* 市民権を得ているUbuntuが使える

## やること
Windows10 に（10分で）WSLを構築しLinux環境を手に入れる

## 環境
Windows10 （Windows Updateは最新の状態にしておく）

## インストール
[シス管系女子 - 漫画でわかるWSL](http://system-admin-girl.com/comic/begins/sp-wsl/)

注） 非常にわかりやすいが、会社で読むには勇気がいるかもしれない。

## インストール（紳士用）
1. **Windows 10 Fall Creators Update (バージョン1709）** へ更新（最新にすればいい）
1. hoge

## 設定
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
