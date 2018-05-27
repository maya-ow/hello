# Homebrew コマンド一覧

## インストール
java と Command Line Tool が必要

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Hombrew/install/master/install)"
```

zsh のコマンド保管設定
"/usr/local/Library/Contribution/" 配下に bash や brew コマンドの補完関数が追加される。それを zsh に読み込ませる。

```
cd /usr/local/share/zsh/site-functions
ln -s ../../../Library/Contributions/brew_zsh_completion.zsh _brew
```

## 用語

formula
パッケージ名のこと。Homebrew では formula と呼ぶ

keg
/usr/local/Cellar/keg/version/

Cellar
デフォルトでは /usr/local/Cellar
インストールしたパッケージの実体は /usr/local/Cellar にあり /usr/local/bin/ や /usr/local/lib/ にシンボリックリンクが作られる

config.log
/Users/<user.name>/Library/Logs/Homebrew/php55 にある

## コマンド

### インストール

```
brew install formula
```

### 検索
'/' でキーワードを囲むと正規表現で検索できる

```
brew search text
brew search /text/
```

### インストール済み formula の一覧

```
brew list
brew -v list
```

### formula のアンインストール

```
brew uninstall formula
```

### 更新のある formula を見る

```
brew outdated
```

