https://ci-labo-omu.github.io/

# Jekyllインストール方法
このHPは[Jekeyll](https://jekyllrb.com/) ([日本語サイト](http://jekyllrb-ja.github.io/)) を使って作成されています．

必ずしもJekyllをインストールしなくても記事の作成/更新等は可能です．ですが，手元のマシンにJekyllをインストールすると更新箇所等の確認ができて便利です．

ここでは，基本的に[Jekyll公式のクイックスタートガイド](https://jekyllrb.com/docs/)に基づいてJekyllをインストールします．
## 1. Rubyのインストール
Jekyllを動かすには[Ruby](https://www.ruby-lang.org/ja/)をインストールする必要があります．手元のマシンに既にRubyをインストールしている場合はこのステップをスキップできます．

ここではマシンに直接Rubyをインストールする方法を紹介します．もし，他にRubyを使った開発を行う予定等がある場合は，[rbenv](https://github.com/rbenv/rbenv)などを経由してRubyをインストール/管理することを検討すると良いでしょう．
### MacOS
ここでは，[Homebrew](https://brew.sh/)経由でインストールする方法を紹介します．状況に応じて適宜読み飛ばし/読み替えなどをしてください．

まず，Homebrewをインストールします．インストール方法は適宜検索してください．

ターミナル上で次のコマンドを入力し，Homebrew経由でRubyをインストールします．
```terminal
brew install ruby
```

ターミナルを再起動し，Rubyがインストールされたことを確認してください．
```terminal
which ruby
/Users/takatokinoshita/.rbenv/shims/ruby

ruby -v
ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [x86_64-darwin21]
```

### Windows
TODO

## 2. Bundlerのインストール
JekyllやHPが依存するgem (Rubyのパッケージ) などをインストールするために[Bundler](https://bundler.io/)をインストールします．BundlerはPythonで言うところのPipenvやPoetryに近いツールです．

ターミナル上で次のコマンドを入力し，`gem`コマンド (Pythonで言うところの`pip`) でBundlerをインストールします．
```
gem install bundler
```

ターミナルを再起動し，Bundlerがインストールされたことを確認してください．
```terminal
bundle -v
Bundler version 2.3.22
```

## 3. HPのソースコードの取得
GithubからHPのソースコードをDLします．
```terminal
git clone https://github.com/ci-labo-omu/ci-labo-omu.github.io.git
```
`./ci-labo-omu`にソースコードがクローンされます．

## 4. Jekyllおよび依存パッケージのインストール
ソースコードをクローンしたディレクトリに移動して，次のコマンドを入力し，Jekyllおよび依存パッケージをインストールします．
```terminal
bundle install
```

Jekyllを実行します．
```
bundle exec jekyll s
```

ブラウザで[http://127.0.0.1:4000](http://127.0.0.1:4000)にアクセスします．  
HPと同じページが表示されていることが確認できれば，インストール成功です．
