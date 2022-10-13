# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


# 質問事項
- Ajax(JavaScript)を利用して、リクエストをルーティングに送る準備をしていたが、なぜかデータが保存されている。この原因がわからない。

## 状況：
- 同期通信から非同期通信へ、Webページを修正しようと準備している段階。
- ボタンを押した時に、イベント発火するかを確認した際、投稿した内容が画面上に表示された。
- レッスンの内容とは異なる状態だったため、一度、SequelProを確認したところ、テーブルに投稿内容が保存されていた。
- 原因がわからず、ひとまずcreateメソッドの内部処理をコメントアウトして対応した。
- しかしレッスンを続けると、最終的にコメントアウトした場所の処理が必要となった。そのため原因を追求しないと、先のレッスンに進めない。

## 調査：
1. 保存されたものが表示されていることから、同期通信がまだ生きていると考えた。
2. HTMLのフォーム内にHTTPメソッドやURLが書き込まれている可能性→書き込まれていたが、レッスンの内容と同じなので、原因ではなさそう。
3. 再度、レッスンの内容を振り返った。→原因の特定できず。
4. サーバーを再起動→問題は解消せず。
5. 考えられる可能性をレッスンのGif画像から検討中。
