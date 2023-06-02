# テーブル設計

## users テーブル
| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false, unique: true |
| email              | string | null: false |
| encrypted_password | text   | null: false |
| profile            | text   | null: false |
| occupation         | text   | null: false |
| position           | text   | null: false |

## prototypes テーブル
| Column             | Type        | Options                       |
| ------------------ | ------      | -----------                   |
| title              | string      | null: false                   |
| catch_copy         | text        | null: false                   |
| user               | references  | null: false, foreign_key:true |


## commentsテーブル
| Column             | Type        | Options                       |
| ------------------ | ------      | -----------                   |
| content            | text        | null: false                   |
| catch_copy         | references  | null: false, foreign_key:true |
| user               | references  | null: false, foreign_key:true |
