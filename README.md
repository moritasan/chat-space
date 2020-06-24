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


## users_テーブル
|Column|Type|Options|
|------|----|-------|
|name|text|null: false, foreign_key: false|
|mail|text|null: false, foreign_key: false|
|pass|integer|null: false, foreign_key: false|
|group_id|integer|null: false, foreign_key: false|

## group_テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: false|
|group_id|integer|null: false, foreign_key: false|

## message_テーブル
|Column|Type|Options|
|------|----|-------|
|message|text|null: false, foreign_key: false|
|text|text|null: false, foreign_key: false|
|image|text|null: false, foreign_key: false|
|user_id|integer|null: false, foreign_key: false|
|group_id|ineteger|null: false, foreign_key: false|


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
