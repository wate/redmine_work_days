# Redmine Work Days Plugin

## イントロダクション

Redmineに個別の休業日の設定を追加するプラグインです。

休業日に設定された日は、Redmine標準の休業日同様に扱われ、ガントチャート上でグレー表示されます。

## 機能

* 管理画面でCSV読み込ませて休業日を設定することができる
* ガントチャート上での休業日を表示することができる  
  休業日を反映するためにはRedmineインスタンスの再起動が必要です。

## インストール方法

以下は `production` 環境でRedmineを動作させている前提です。

### Gitを使う

```
$ cd [Redmine Root]
$ git clone git@github.com:agileware-jp/redmine_work_days.git plugins/redmine_work_days
$ bundle install
$ RAILS_ENV=production bundle exec rake redmine:plugins:migrate NAME=redmine_work_days
```

### ZIPファイルを使う

1. [Download ZIP]を押下する
2. ZIPファイルを解凍する
3. ディレクトリ名を「redmine_work_days」に変更する
4. プラグインを配備する  
  以下に「redmine_work_days」を配備する。

  ```
  [Redmine Root]/plugins
  ```

5. プラグインをインストールする

  ```
  $ bundle install
  $ RAILS_ENV=production bundle exec rake redmine:plugins:migrate NAME=redmine_work_days
  ```

## アンインストール方法

以下は `production` 環境でRedmineを動作させている前提です。

```
$ cd [Redmine Root]
$ RAILS_ENV=production bundle exec rake redmine:plugins:migrate NAME=redmine_work_days VERSION=0
$ rm -rf plugins/redmine_work_days
```

## About

Copyright (c) 2015 [Agileware Inc.](http://agileware.jp) released under the MIT license
