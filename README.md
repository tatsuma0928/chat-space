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
|user_name|string|null: false,unique: true|

## massagesテーブル
|column|Type|Options|
|------|----|-------|
|message|text|null: false, foreign_key: true|
|image|text|foreign_key: true|

## groupsテーブル
|column|Type|Options|
|------|----|-------|
|group_name|string|null: false, foreign_key: true, unique: true|

## groups_usersテーブル
|column|Type|Options|
|------|----|-------|
|group_name|string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user




* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
