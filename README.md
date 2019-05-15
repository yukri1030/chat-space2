
# README



## usersテーブル
|Column|Type|Opitions|
|------|----|---------|


### Asociation
- has_many :groups , through :member
- has_many :messages


## groupテーブル

|Column|Type|Opitions|
|------|----|---------|
|id|integer|null:false, foreign_key: true｜
|name|string|null: false,uniqe:true|
|member_id|integer|null:false, foreign_key: true|

### Asociation
- has_many: members through: users

## memberテーブル

|Column|Type|Opitions|
|------|----|---------|
|id|integer|null:false, foreign_key: true|
|user_id|reference|null: false,foreign_key :true|
|group_id|integer|null:false, foreign_key: true|


- belongs_to: group 
- belongs_to: user
- has_many: messages


## messageテーブル

|Column|Type|Opitions|
|------|----|---------|
|id|integer|null:false, foreign_key: true｜
|message|text|
|img|string|

### Association

- belongs_to: user 
- belongs_to: member


