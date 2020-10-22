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

<<<<<<< Updated upstream
=======


>>>>>>> Stashed changes
# テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name     | string | null: false |
| email    | string | null: false |
| password | string | null: false |

### Association
<<<<<<< Updated upstream
-  has_many :saves
-  has_one  :points
-  has_many :uses

## saves テーブル

| Column      | Type        | Options     |
| ------      | ------      | ----------- |
| dead_line   | string      | null: false |
| save_point  | integer     | null: false |
| done        | boolean     | null: false |

### Association
-  belongs_to :users

## points テーブル

| Column        | Type       | Options                        |
| ------        | ---------- | ------------------------------ |
| user_points   | references | null: false, foreign_key: true |

### Association
-  belongs_to :users

## uses テーブル

| Column     | Type       | Options     |
| -------    | ---------- | ----------- |
| use_name   | string     | null: false |                  
| use_point  | integer    | null: false |            
| done       | boolean    | null: false |

### Association
- belongs_to :users
=======

- has_many :room_users
- has_many :rooms, through: room_users
- has_many :messages

##  savesテーブル

| Column      | Type     | Options     |
| ------      | ------   | ----------- |
| dead_line   | datetime | null: false |
| save_point  |          |                |
| done        |          |             |

### Association

- has_many :room_users
- has_many :users, through: room_users
- has_many :messages

##  usesテーブル

| Column          | Type       | Options                        |
| ------          | ---------- | ------------------------------ |
| use_name        | string     | null: false |
| use_point       |  | null: false |

### Association

- belongs_to :room
- belongs_to :user

##  pointsテーブル

| Column     | Type        | Options                        |
| -------    | ----------  | ------------------------------ |
| user_point | references  | null: false, foreign_key: true |

### Association

- belongs_to :room
>>>>>>> Stashed changes
