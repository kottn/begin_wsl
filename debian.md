# Debian にする

再起動が完了したら、
1. [Microsoft Store - Debian GNU/Linux](https://www.microsoft.com/ja-jp/store/p/debian-gnu-linux/9msvkqc78pk6?activetab=pivot%3aoverviewtab) にアクセス（もしくは Microsoft Store を開き "Debian" と検索）。
1. 入手。
1. Debian を起動する。
1. 初回起動はコマンド類のインストールに時間がかかる。
1. 名前の設定を促されるので設定。（Windowsのユーザー名にそろえるとよい）
1. パスワード設定を促されるので設定。
1. 完了後、以下を実行。バージョンが見れるはずである。
```
$ cat /etc/os-release
```

## 初期設定
### リポジトリ参照先の変更
1. 国内ミラーの有効化。
```
$ cd /etc/apt/sources.list.d \
        && sudo curl -LO https://raw.githubusercontent.com/kottn/begin_wsl/master/jpdebian.list
```
1. デフォルト（`deb.debian.org`）の無効化。
```
$ sudo vi /etc/apt/sources.list
```
全部コメントアウトする。
```
# deb http://deb.debian.org/debian stretch main
# deb http://deb.debian.org/debian stretch-updates main
# deb http://security.debian.org/debian-security/ stretch/updates main
```

* 仕上げ
```
$ sudo apt update
$ sudo apt upgrade
```

### X の設定 :eyes:
```
$ sudo apt install ???
$ echo "export DISPLAY=localhost:0.0" >> ~/.bash_profile
$ source ~/.bash_profile
$ xeyes
```
あらかじめ Windows 側で Xming等 を起動してればおめめがでてくるはず。

### とりあえず入れておくパッケージ達
```
$ sudo apt install \
    ssh \
    build-essential \
    gfortran \
    vim \
    git \
    manpages-ja \
    manpages-ja-dev \
    tree \
    less \
    gnuplot5-x11 \
    bash-completion
```
これで必要最低限の設定は終わりです。

[便利な設定へ](./finish.md)

[はじめにもどる](./README.md)

