## Table名

|Column|Type|Options|
|------|----|-------|
（ここに追記していく）

## users table
has_many :music
has_many :comments
has_many :order

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false, unique: true|
|email|string|null: false, unique: true|
|encrypted_password|string|null: false|

## musics table
belongs_to :user
has_many :comments
has_many :order

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|title|string|null: false|
|detail|text|null: false|
|genre_id|integer|null: false|
|price|integer|null: false|

## comments table
  belongs_to :music
  belongs_to :user

|Column|Type|Options|
|------|----|-------|
|music_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|comment|integer|null: false|

## orders table
belongs_to :user
belongs_to :music
has_one :address

|Column|Type|Options|
|------|----|-------|
|music_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

## addresses table
belongs_to :order

|Column|Type|Options|
|------|----|-------|
|postal_code|string|null: false|
|prefecture_id|integer|null: false|
|city|string|null: false|
|house_number|string|null: false|
|building_name|string|
|phone_number|string|null: false|
|customer_id|integer|null: false, foreign_key: true|

### Association
（ここに追記していく）