---
date: "2020-08-21"
title: "Laravel 学習メモ"
---

# データベース関連

## シーディング
テストデータやマスタデータなどのアプリケーション起動時に必要なデータをコマンドで登録する仕組み。シーダーファイルと呼ばれる php のソースコードに登録するデータを記述し実行することでレコードが登録される。

### シーダーファイルを作成する
```$ php artisan make:seeder```
シーダーファイルの run メソッドに登録するデータやテーブル操作を記述する。

### シーディングを実行する
```$ php artisan db:seed```
コマンドを実行することでテーブルにデータが登録される。

## マイグレーション

### PK の設定
id メソッドを使わない場合は primary メソッドを使用することで PK を設定できる。
```php
Schema::create('books', function (Blueprint $table) {
    $table->integer('FARM_ID')->primary();
```

# コントローラー関連

## ルーティング

### RESTful なルーティング
```php
// resource メソッドひとつで CRUD 画面用のメソッドとマッピングされる
Route::resource('hoge', 'HogeController');
```
