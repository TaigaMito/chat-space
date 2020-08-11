# README

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|string|null: false, foreign_key: true|
|password|string|null: false, foreign_key: true|
|nickname|string|null: false, foreign_key: true|

### アソシエーション

- has_many :messages, through: :groups_users
- has_many :groups_users
- belongs_to :group

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null :false, foreign_key: true|
|groupname|string|null :false, foreign_key: true|

###　アソシエーション

- has_many :users, through: :groups_users
- has_many :groups_users
- has_many :messages


## messageテーブル

|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text||
|user_id|integer|null: false, foreign_key: true|

### アソシエーション

- belongs_to :user
- belongs_to :group

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### アソシエーション

- belongs_to :user
- belongs_to :group
