
# README



## usersテーブル
|Column|Type|Opitions|
|------|----|---------|
|id|integer|null:false, foreign_key: true|
|------|----|---------|
|name|string|nill:false, foreign_key: true, uniqe:true|
|e-mail|varchar(30)|null:false|
|message_id|null:false, foreign_key: true|
|member_id|integer|null:false, foreign_key: true|

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
|user_id|string|null: false,foreign_key :true|
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


