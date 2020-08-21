---
date: "2020-08-21"
title: "Laravel 学習メモ"
---

# Laravel 学習メモ

## シーディング
テストデータやマスタデータなどのアプリケーション起動時に必要なデータをコマンドで登録する仕組み。シーダーファイルと呼ばれる php のソースコードに登録するデータを記述し実行することでレコードが登録される。

### シーダーファイルを作成する
```$ php artisan make:seeder```
シーダーファイルの run メソッドに登録するデータやテーブル操作を記述する。

### シーディングを実行する
```$ php artisan db:seed```
コマンドを実行することでテーブルにデータが登録される。