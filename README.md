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
|name|string|null: false, unique: true|

### Association
- has_many :messages
- has_many :groups, through :users_groups
- belong_to :users_groups

## massagesテーブル
|column|Type|Options|
|------|----|-------|
|text|text||
|image|text||
|user_id|integer|null: false, foreign_key: true|
|group_id||integer|null: false, foreign_key: true|
### Association
- belong_to :user
- belong_to :group

## groupsテーブル
|column|Type|Options|
|------|----|-------|
|name|string|null: false, unique: true|

### Association
- has_many :users, through :users_groups
- belong_to :users_groups
- has_many :messages

## groups_usersテーブル
|column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id||integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user




* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
