# README

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|string|null: false, foreign_key: true|
|password|string|null: false, foreign_key: true|
|nickname|string|null: false, foreign_key: true|

### アソシエーション

- has_many :posts
- belongs_to :groups

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null :false, foreign_key: true|
|groupname|string|null :false, foreign_key: true|

###　アソシエーション

- has_many :users


## messageテーブル

|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text||
|user_id|integer|null: false, foreign_key: true|

### アソシエーション

- belongs_to :users

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### アソシエーション

- belongs_to :user
- belongs_to :group




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
