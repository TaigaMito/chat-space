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

- belongs_to :users
- belongs_to :groups
