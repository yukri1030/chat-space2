
# README



## usersテーブル
|Column|Type|Opitions|
|------|----|---------|
|name|string|null: false,uniqe:true|
|messages_id|reference|null: false,foreign_key :true|


### Asociation
- has_many :groups , through :members
- has_many :messages
- has_many：members

## groupテーブル

|Column|Type|Opitions|
|------|----|---------|
|name|string|null: false,uniqe:true|
|messages_id|reference|null: false,foreign_key :true|


### Asociation
- has_many: users through: members
- has_many: messages through: users

## memberテーブル

|Column|Type|Opitions|
|------|----|---------|
|user_id|reference|null: false,foreign_key :true|
|group_id|reference||null:false, foreign_key: true|
|message_id|reference|null: false,foreign_key :true|


- belongs_to: group 
- belongs_to: user



## messageテーブル

|Column|Type|Opitions|
|------|----|---------|
|user_id|reference|null: false,foreign_key :true|
|group_id|reference||null:false, foreign_key: true|
|message|text|
|img|string|

### Association

- belongs_to: user 
- belongs_to: group

