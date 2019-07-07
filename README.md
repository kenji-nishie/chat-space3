# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation
## userテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|e-mail|integer|null: false|

### Association
- has_many :menbers
- has_many :group, through: :menbers

## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|image|string|
|body|text|null: false|

### Association
- belongs_to :group
- belongs_to :user

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group-name|string|null: false|
|menber_name|string|null: false|

### Association
- has_many :menbers
- has_many :user, through: :menbers


* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
