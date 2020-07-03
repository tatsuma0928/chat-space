# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation
## usersテーブル
|column|Type|Options|
|------|----|-------|
|name|string|null: false, foreign_key: true, unique: true|

### Association
- has_many :messages
- belong_to :user_id

## massagesテーブル
|column|Type|Options|
|------|----|-------|
|message|text|null: false|
|image|text||

### Association
- belong_to

## groupsテーブル
|column|Type|Options|
|------|----|-------|
|name|string|null: false, foreign_key: true, unique: true|

### Association
- belong_to :group_id

## groups_usersテーブル
|column|Type|Options|
|------|----|-------|
|user_id|string|null: false, foreign_key: true|
|group_id||string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user




* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
